# Guessing-Game
Focuses solely on selection and repetition structures.


Scenario: This program prompts the user to play a game titled “Champions League Winner Guessing Game”, and focuses mainly on
using selection and repetition structures. In this game, the user has to guess which English city won the 2023 Champions League
title, and is given a hint by the program that the city is 10 characters long. The user has 10 attempts to successfully guess the city,
either through entering individual characters of the word, or entering the complete word itself.

Input:
- 10 characters word of the guessed answer
- OR 10 individual characters each attempt to guess the answer
- At the end, the user is asked if they want to play again
- Input: response to the question above

Algorithm:
1. Display the game introduction and rules.
2. Initialize the game variables:
- Set the secretWord variable to "Manchester".
- Set the guessedWord variable to an empty string.
- Set the attempts variable to 10.
3. Start a game loop that continues until the number of attempts is zero or the guessed word matches the secret word:
a. Display the number of attempts remaining.
b. Prompt the user to enter a letter or the full word.
c. Read the user's input.
d. If the input is a single character:
- Check if the character is present in the secretWord:
- If it is present, add the character to the guessedWord.
- If it is not present, display an incorrect guess message and reduce the attempts by 1
e. If the input is a word:
- Check if the word matches the secretWord:
- If it matches, assign the secretWord to the guessedWord.

- If it does not match, display an incorrect guess message and reduce the attempts by 1
f. If the input is invalid (not a single character or a word), display an invalid input message.
4. After the game loop ends:
a. Check if the guessedWord matches the secretWord:
- If it matches, display a congratulations message.
- If it does not match, display an out of attempts message and reveal the secretWord.
b. Ask the user if they want to play again.
c. Read the user's response.
d. If the response is "Yes", go back to step 3 (aka start the lop again).
e. If the response is "No", end the game.
5. Display a thank you message for playing the game.
6. End the program

  
Process/Predefined Methods used:
● String guess = input.nextLine().toLowerCase(); - Reads a line of input from the user and converts it to lowercase. It is used to
get the user's guess.
● guess.length() - Returns the length of the guess entered by the user. It is used to check if the guess is a single letter or the full
word.
● guess.charAt(0) - Gets the fist character of the guess. It is used when the user guesses a single letter.
● secretWord.toLowerCase().indexOf(guess) != -1 - Checks if the guess (a letter) is present in the secretWord.
- The indexOf() method returns the index of the first occurrence of the specified character in the string
● guessedWord += letter - Assigns the guessed letter to the guessedWord. It is used when the user guesses a single letter
correctly.
● guess.equalsIgnoreCase(secretWord) - Checks if the guess (the full word) is equal to the secretWord, ignoring case.

● response = input.nextLine().toLowerCase(); - Reads the user's response (whether they want to play again) and converts it to
lowercase.
