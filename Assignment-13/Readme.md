
Create a program that prompts the user to input scoring totals for 5 players during 4 basketball games. The program will track which player had the highest scoring average over the 4 games and print the result to the terminal.

Hint: Use a two-dimensional array and nested for loops. The outer-most for loop will iterate on a per game basis gathering scores for the inner-most for loop interating through players. Use this same model to create arrays to store total scores and to calculate averages.

-------


#### CODE

###InProgress

```
#include <stdio.h>

int main() {
    // Define constants for the number of players and games
    const int numPlayers = 5;
    const int numGames = 4;

    // Declare a two-dimensional array to store scores
    int scores[5][4];

    // Prompt the user to input scores for each player and game
    for (int i = 0; i < numPlayers; i++) {

        printf("Enter scores for Player %d (4 games):\n", i + 1);

        for (int j = 0; j < numGames; j++) {
            printf("Game %d: ", j + 1);
            scanf_s("%d", &scores[i][j]);
        }
    }

    // Calculate the total scores for each player and the highest average
    int highestAverage = 0;
    int playerWithHighestAverage = 0;

    for (int i = 0; i < numPlayers; i++) {
        int totalScore = 0;
        for (int j = 0; j < numGames; j++) {
            totalScore += scores[i][j];
        }

        // Calculate the average for the current player
        int average = totalScore / numGames;

        // Check if the current player has a higher average
        if (average > highestAverage) {
            highestAverage = average;
            playerWithHighestAverage = i;
        }
    }

    // Display the player with the highest average
    printf("Player %d has the highest scoring average of %d\n", playerWithHighestAverage + 1, highestAverage);

    return 0;
}


```
