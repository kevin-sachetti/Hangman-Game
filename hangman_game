# Hangman Game

# Import
import random
from os import system, name

# Clear the screen
def clear_screen():
 
    # Windows
    if name == 'nt':
        _ = system('cls')
 
    # Mac ou Linux
    else:
        _ = system('clear')

# Function
def game():

    clear_screen()
    print("\Welcome to Hangman game!")
    print("Guess the word below, it's an animal!:\n")

    # List of words
    words = ['alligator', 'fish', 'frog', 'monkey', 'cat', 'dog']
    
    # Choose at random word
    word = random.choice(words)

    # List comprehension
    discovered_letters = ['_' for letter in word]

    # Number of chances
    chances = 6

    # List for wrong letters
    wrong_letters = []

    # Loop for the chances
    while chances > 0:

        # Print
        print(" ".join(discovered_letters))
        print("\nRemaining chances:", chances)
        print("Wrong letters:", " ".join(wrong_letters))

        # Attempt
        attempt = input("\nType a letter: ").lower()

        # Conditional
        if attempt in word:
            index = 0
            for letter in word:
                if attempt == letter:
                    discovered_letters[index] = letter
                index += 1
        else:
            chances -= 1
            wrong_letters.append(attempt)

        # Conditional
        if "_" not in discovered_letters:
            print("\nCongrats! You won!The word was:", word)
            break

    # Conditional
    if "_" in discovered_letters:
        print("\nYou lost... The word was:", word)

# main
if __name__ == "__main__":
    game()
    print("\nCongratulations, you're learning animal names :D\n")
