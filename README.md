import random
def get_computer_choice():
    return random.choice(["rock","scissor","paper"])
def get_winner(player, computer):
    if player == computer:
        return "It's a Tie"
    elif (player == "rock" and computer == "scissor") or \
         (player == "scissor" and computer == "paper") or \
         (player == "paper" and computer == "rock"):
        return "You Won"
    else:
        return "Computer Won"
    
def play_game():
    print("Welcome to the Game")
    while True:
        player_choice = input("Enter rock, scissor or paper (or type quit to exist): ").lower()

        if player_choice == "quit":
            print("Thank you for playing")
            break
        elif player_choice not in ["rock", "scissor", "paper"]:
            print("Invalid commmand. Please type rock, scissor or paper to play")

        computer_choice = get_computer_choice()
        print(f"computer choose: {computer_choice}")
        print(get_winner(player_choice, computer_choice))


if __name__ == "__main__":
    play_game()
