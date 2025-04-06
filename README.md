#-------------Rock/Paper/scissor----------------GAME
import random

#3 verievals for count--win,lose,tie--

user_win=0
computer_win=0
tie=0

options=["rock","paper","scissor"]

#we will run loop

while True : 

    #take input for chose and quiit--
    user=input("Type (ROCK/PAPER/SCISSOR) OR (Q-Quit): ").lower()

    if user=="q":
        break

    #we will use (not in) if user type invalid input--exept-(rock,paper,scissor)

    if user not in ["rock","paper","scissor"]:
        print("...Invalid Choice,Try Again...")
        continue

    #function to choice rock/paper/scissor--computer will chossee

    random_num=random.randint(0,2)#rock:0 , paper:1 ,scissor:2
    computer_pic=options[random_num]
    print(f"Computer Picked {computer_pic}.")

    #conditin 

    if user == "rock" and computer_pic == "scissor":
        print("---YOU WON---")
        user_win+=1
        continue

    elif user == "rock" and computer_pic == "rock" :
        print("--TIE--")
        tie+=1
        continue

    if user == "scissor" and computer_pic == "paper":
        print("---YOU WON---")
        user_win+=1
        continue

    elif user == "paper" and computer_pic == "paper" :
        print("--TIE--")
        tie+=1
        continue

    if user == "paper" and computer_pic == "rock":
        print("---YOU WON---")
        user_win+=1
        continue

    elif user == "scissor" and computer_pic == "scissor" :
        print("--TIE--")
        tie+=1
        continue

    else:
        print("---YOU LOST---")
        computer_win+=1

print(f"You won {user_win} Times..")
print(f"The Computer Won {computer_win} Times..")
print(f"Tie {tie} Times..")
print(f"PROGRAM ENDING.......")
print(f"----GOODBYE----")
