import random

def rps():
    choices = ["rock", "paper", "scissors"]
    score_user = 0
    score_device = 0

    while True:
        print("\n------------------Play And Enjoy-------------------------\n")
        print("Enter 'rock', 'paper', or 'scissors' for choice.")
        print("Enter '0' to stop playing.")
        user_choice = input("Enter your choice: ").lower()

        if user_choice == "quit":
            break

        if user_choice not in choices:
            print("Invalid choice. Please try again.")
            continue

        Device_choice = random.choice(choices)
        print(f"\nYou chose: {user_choice}")
        print(f"Device chose: {Device_choice}")

        if user_choice == Device_choice:
            print("It's a tie!")
        elif (user_choice == "rock" and Device_choice == "scissors") or \
             (user_choice == "scissors" and Device_choice == "paper") or \
             (user_choice == "paper" and Device_choice == "rock"):
            print("You won!")
            score_user += 1
        else:
            print("You failed")
            score_device += 1

        print(f"Score - You: {score_user}, Device: {score_device}")
print("\nWell played ")

rps()
