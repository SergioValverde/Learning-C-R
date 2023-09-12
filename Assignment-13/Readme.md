
Create a program that prompts the user to input scoring totals for 5 players during 4 basketball games. The program will track which player had the highest scoring average over the 4 games and print the result to the terminal.

Hint: Use a two-dimensional array and nested for loops. The outer-most for loop will iterate on a per game basis gathering scores for the inner-most for loop interating through players. Use this same model to create arrays to store total scores and to calculate averages.

-------


#### CODE

###InProgress

```
#include <stdio.h>



int main(void) {

	//array de 5 elementos (players) of 4 elements (games) de tipo int;

	int players[5][4];
	int score[5];
	

	// 
	int games_counter,player_counter;


	for (games_counter = 0; games_counter < 4; games_counter++) {

		
		for (player_counter = 0; player_counter < 5; player_counter++) {
			
			//printf("Enter the scopre for every player: \n");
			scanf_s("%d", players[j][i]);

			printf("The score is: %d", players[j][i]);

		}

		
	}


	return 0;
}

```
