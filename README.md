# Guess-the-number

import random

def hard():
    print("Welcome to the number guessing game")
    print("Guess a number between 1 to 100")
    c=random.randint(0,101)
    print(c)
    life=5
    while life>0:
        d=int(input("Enter a number: "))
        if d!=c:
            if d>c:
                print("You are ahead the number")
                print(f"You have {life-1} left")
            elif d<c:
                print("You are behind the number")
                print(f"You have {life-1} left")
            life-=1
            if life ==0:
                print("You lose the game")
        else:
            print("Congratulations! You have guessed the number correctly")

def easy():
    print("Welcome to the number guessing game")
    print("Guess a number between 1 to 50")
    c=random.randint(0,51)
    print(c)
    life=10
    while life>0:
        d=int(input("Enter a number: "))
        if d!=c:
            if d>c:
                print("You are ahead the number")
                print(f"You have {life-1} left")
            elif d<c:
                print("You are behind the number")
                print(f"You have {life-1} left")
            life-=1
            if life ==0:
                print("You lose the game")
        else:
            print("Congratulations! You have guessed the number correctly")


print("What is the level of the Game")
a=input("Hard(h) and easy(e): ")
a=a.lower()
if a == "h":
    hard()
elif a=="e":
    easy()
else:
    print("Invalid input....")
