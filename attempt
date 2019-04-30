import random

words_list = ["orion", "quark", "quasar", "python", "bigbang"]
accepted_input = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']
word_guess = random.choice(words_list)
word_to_guess = []
for i in range(0, len(word_guess)):
    word_to_guess.append(word_guess[i])
currently = []
for i in word_to_guess:  # fill in our currently guessed list with "_"
    currently.append("_")
guess_letters = []
guesses = 0


def hangman_graphic(guesses):
    print("")
    print("Currently you know: ", end=" ")
    for i in range(0, len(currently)):
        print(currently[i], end=" ")
    print("")
    print("You have already tried letters:", end=" ")
    for i in range(0, len(guess_letters)):
        print(guess_letters[i], end=" ")
    print("")
    if guesses == -1: # you won graphic
        print("       0      ")
        print("     ~~|~~    ")
        print("      / \     ")
        print("You won!")
    elif guesses == 0:
        print("________      ")
        print("|      |      ")
        print("|             ")
        print("|             ")
        print("|             ")
        print("|             ")
    elif guesses == 1:
        print("________      ")
        print("|      |      ")
        print("|      0      ")
        print("|             ")
        print("|             ")
        print("|             ")
    elif guesses == 2:
        print("________      ")
        print("|      |      ")
        print("|      0      ")
        print("|     /       ")
        print("|             ")
        print("|             ")
    elif guesses == 3:
        print("________      ")
        print("|      |      ")
        print("|      0      ")
        print("|     /|      ")
        print("|             ")
        print("|             ")
    elif guesses == 4:
        print("________      ")
        print("|      |      ")
        print("|      0      ")
        print("|     /|\     ")
        print("|             ")
        print("|             ")
    elif guesses == 5:
        print("________      ")
        print("|      |      ")
        print("|      0      ")
        print("|     /|\     ")
        print("|     /       ")
        print("|             ")
    else:   # you lost graphic
        print("________      ")
        print("|      |      ")
        print("|      0      ")
        print("|     /|\     ")
        print("|     / \     ")
        print("|             ")
        print("You lost!")

def guess_input():
    global guesses
    global currently
    global word_to_guess

    while True:
        user_input = input("Please input your guess (a single letter): ")
        if user_input in accepted_input:
            if user_input in guess_letters:
                print("Try again")
            else:
                guess_letters.append(user_input)
                if user_input in word_to_guess:
                    print("Good guess")
                    for i in range(0, len(word_to_guess)):
                        if word_to_guess[i] == user_input:
                            currently[i] = user_input
                else:
                    print("Guess a letter")
                    guesses = guesses + 1

        else:
            print("INPUT ERROR! Please input single letter in range a-z")

        if guesses > 5: #game over you lost
            hangman_graphic(guesses)
            break
        elif "_" in currently: #keep playing
            hangman_graphic(guesses)
        else: #game over you WON
            hangman_graphic(-1)
            break


def hangman():
    hangman_graphic(guesses)
    guess_input()


if __name__ == "__main__":
    hangman()
    print("The End")
