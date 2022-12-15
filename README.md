# Rock-Paper-Scissors
This is a basic "Rock Paper Scissors" game programmed in Python. 
Learned: importing libraries, creating lists, calling methods, creating functions

import random


def get_choices():
    # player
    player_choice = input("Enter a choice (rock, paper, scissors): ")

    # computer
    computer_options = ["paper", "rock", "scissors"]
    computer_choice = random.choice(computer_options)
    choices = {"player": player_choice, "computer": computer_choice}
    return choices


def check_win(player, computer):
    print(f"You chose {player}, the computer chose {computer}.")

    # tie
    if player == computer:
        return "It's a tie! 😑"
    
    # rock
    elif player == "rock":
        if computer == "paper":
            return "Paper covers rock! You lose. 😥"
        else:
            return "Rock smashers scissors! You win! 😁"
            
    # paper
    elif player == "paper":
        if computer == "scissors":
            return "Scissors destroy paper! You lose! 😥"
        else:
            return "Paper covers rock! You win! 😁"
    # scissors
    elif player == "scissors":
        if computer == "rock":
            return "Rock smashers scissors! You lose. 😥"
        else:
            return "Scissors destroy paper! You win! 😁"


choices = get_choices()
result = check_win(choices["player"], choices["computer"])
print(result)
