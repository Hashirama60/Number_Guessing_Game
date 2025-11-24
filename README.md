# Number Guessing Game (Python)

This project is a simple, beginner-friendly **Number Guessing Game** written in Python. The computer randomly selects a number between **1 and 100**, and the player must guess it. After each guess, the program provides feedback on whether the guess was **too high**, **too low**, or **correct**.

---

## 🎮 How the Game Works

1. The program generates a random number using Python's `random` module.
2. The player enters a guess.
3. The game checks:

   * If the guess is **too high** → it prompts the player to try again.
   * If the guess is **too low** → it prompts the player to try again.
   * If the guess is **correct** → the game displays a success message.
4. The game keeps track of the number of attempts.

---

## 🧠 Concepts Used

* Variables
* Loops (`while` loop)
* Conditional statements (`if/elif/else`)
* Random number generation
* Input handling
* Exception handling (`try/except`)

---

## 🚀 How to Run the Program

1. Install Python 3 if you haven’t already.
2. Save the game code in a file named `number_guessing_game.py`.
3. Open a terminal or command prompt.
4. Run the script with:

   ```bash
   python number_guessing_game.py
   ```

---

## 🧩 Full Source Code

```python
import random

def number_guessing_game():
    print("Welcome to the Number Guessing Game!")
    print("I'm thinking of a number between 1 and 100.")

    # Generate a random number between 1 and 100
    secret_number = random.randint(1, 100)
    attempts = 0

    while True:
        try:
            guess = int(input("Enter your guess (1–100): "))
        except ValueError:
            print("Please enter a valid integer.")
            continue

        if guess < 1 or guess > 100:
            print("Your guess must be between 1 and 100!")
            continue

        attempts += 1

        if guess < secret_number:
            print("Too low! Try again.")
        elif guess > secret_number:
            print("Too high! Try again.")
        else:
            print(f"🎉 Correct! The number was {secret_number}.")
            print(f"You guessed it in {attempts} attempts.")
            break

if __name__ == "__main__":
    number_guessing_game()
```

---

## 📌 Possible Improvements

* Add difficulty levels (Easy, Medium, Hard)
* Limit the number of attempts
* Provide hints (e.g., "You’re very close!")
* Create a GUI with Tkinter

---

## 📜 License

This project is free to use for learning and practice. Feel free to modify it!
