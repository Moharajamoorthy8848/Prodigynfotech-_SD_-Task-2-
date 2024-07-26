```python
import random

def number_guessing_game():
    print("Welcome to the Number Guessing Game!")
    
    number_to_guess = random.randint(1, 100)
    attempts = 0
    
    while True:
        user_guess = input("Guess a number between 1 and 100: ")
        
        try:
            user_guess = int(user_guess)
        except ValueError:
            print("Please enter a valid number.")
            continue
        
        attempts += 1
        
        if user_guess < number_to_guess:
            print("Too low! Try guessing higher.")
        elif user_guess > number_to_guess:
            print("Too high! Try guessing lower.")
        else:
            print(f"Congratulations! You guessed the correct number in {attempts} attempts.")
            break

number_guessing_game()
```
