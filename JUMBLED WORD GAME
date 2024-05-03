import random

# Function to choose a random word from the file
def choose():
    with open("demofile.txt", "r") as file:
        words = file.readlines()
    pick = random.choice(words).strip()  # Remove newline character
    return pick

# Function to shuffle the characters of the chosen word
def jumble(word):
    random_word = random.sample(word, len(word))
    jumbled = ''.join(random_word)
    return jumbled

# Function to show final score
def thank(p1n, p2n, p1, p2):
    print(p1n, 'Your score is :', p1)
    print(p2n, 'Your score is :', p2)
    check_win(p1n, p2n, p1, p2)
    print('Thanks for playing...')

# Function to declare winner
def check_win(player1, player2, p1score, p2score):
    if p1score > p2score:
        print("Winner is:", player1)
    elif p2score > p1score:
        print("Winner is:", player2)
    else:
        print("Draw. Well Played!")

# Function to play the game
def play():
    p1name = input("Player 1, please enter your name: ")
    p2name = input("Player 2, please enter your name: ")
    pp1 = 0
    pp2 = 0
    turn = 0

    while True:
        picked_word = choose()
        qn = jumble(picked_word)
        print("Jumbled word is:", qn)

        if turn % 2 == 0:
            print(p1name, 'HEY Its Your Turn.')
            ans = input("What is in your mind? ")

            if ans == picked_word:
                pp1 += 1
                print('Your score is:', pp1)
            else:
                print("OOPS!!!! Better luck next time..")
                print(p2name, 'HEY Its Your turn.')
                ans = input('What is in your mind? ')

                if ans == picked_word:
                    pp2 += 1
                    print("Your Score is:", pp2)
                else:
                    print("OOPS!!!! Better luck next time... Correct word is:", picked_word)
                    c = int(input("Press 1 to continue and 0 to quit: "))
                    if c == 0:
                        thank(p1name, p2name, pp1, pp2)
                        break
        else:
            print(p2name, 'HEY Its Your turn.')
            ans = input('What is in your mind? ')

            if ans == picked_word:
                pp2 += 1
                print("Your Score is:", pp2)
            else:
                print("OOPS!!! Better luck next time.. :")
                print(p1name, 'HEY Its Your turn.')
                ans = input('What is in your mind? ')

                if ans == picked_word:
                    pp1 += 1
                    print("Your Score is:", pp1)
                else:
                    print("OOPS!!!! Better luck next time... Correct word is:", picked_word)
                    c = int(input("Press 1 to continue and 0 to quit: "))
                    if c == 0:
                        thank(p1name, p2name, pp1, pp2)
                        break

        turn += 1

if __name__ == "__main__":
    play()
