import os
import random

def choose_secret_word(word_bank):    # choosing a secret word for the word bank
    return random.choice(word_bank).lower()

def take_turn(secret_word, guesses_left, word_guesses_left):    # managing the players turn 
    print(f"Guess the word! You have {guesses_left} letter guesses and {word_guesses_left} word guesses left.")
    while guesses_left > 0 or word_guesses_left > 0:
        guess = input("Enter a letter or guess the whole word: ").lower()

        if len(guess) == 1:  # The letter guesses 
            if guess in secret_word:
                occurrences = secret_word.count(guess)
                print(f"Correct! The letter '{guess}' appears {count} times.") 
            else:
                print("Incorrect!")
            guesses_left -= 1
        elif guess == secret_word:
            print("Congrats! You guessed the word right!")
            return
        else:
            word_guesses_left -= 1
            if word_guesses_left == 0:
                print(f"Game Over! You've used all your word guesses. The word was '{secret_word}'.")
                return
            else:
                print("This is wrong. Try again!")

        print(f"You have {guesses_left} letter guesses and {word_guesses_left} word guesses left.")
        if guesses_left == 0:
            print(f"Oops, you've run out of guesses. The word was: {secret_word}")
            return


def main():    # the game loop 
    word_bank = ["Nike", "Adidas", "Puma", "Lululemon", "Sketchers"]
    secret_word = choose_secret_word(word_bank)
    guesses_left = 5
    word_guesses_left = 3
    take_turn(secret_word, guesses_left, word_guesses_left)




