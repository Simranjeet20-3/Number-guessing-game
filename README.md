# Number-guessing-game
A simple number guessing game
#include<stdio.h>
#include<stdlib.h>
#include<time.h>
int main(){
	int random ,guess;
	int no_of_guess;
	printf("Welcome to the world of guessing numbet\n");
	random = rand()%100+1;
	
	do{
		printf("please enter your guess(between 1 to 100):");
		scanf("%d",& guess);
		no_of_guess++;
		srand(time(NULL));
		if(guess<random){
			printf("guess a larger number\n");
		}else if(guess>random){
		printf("guess a smaller number\n");
		} else{
			printf("Congratulations!!! you have succesfully guessed correct number in %d attempts\n",no_of_guess);
		}
	}while (guess!= random);
	printf("BYE BYE!! Thanks for playing the game\n");
	printf("Developed by SIMRANJEET\n");
	return 0;
}
