# Homework – Loops

Solve at least one question (recommended: try all) using Python code

## Question 1 – Safe Code

You are given a secret code:

`[77, 12, 43, 100, 51]`

Goal: the user must enter the numbers exactly in the correct sequence

Rules:

* Go through the secret code in order
* Each time, the user enters one number
* If the number is correct → move to the next number
* If the user makes even ONE mistake → reset progress and start again from the beginning
* The loop only ends when the full sequence is entered correctly

Example:

`4, 10, 77, 12, 43, 77`

Explanation:

* `4` → wrong
* `10` → wrong
* `77` → correct (start)
* `12` → correct
* `43` → correct
* `77` → wrong → reset to start

Hint:

* Use an index variable to track your position in the code
* Reset the index to 0 when there is a mistake

## Question 2 – Casino Slot Machine

Starter code:

```python
rate    = [2,    3,    9,      7,     11 ]
symbols = ["🍒", "🍋", "⭐", "🔔", "💎"]
money = 50
print("=== SLOT MACHINE === \n")
```

Goal: build a slot machine with 3 spinning slots

Rules:

* Each spin shows 3 random symbols
* The player starts with `50` money
* Before each spin, ask the user how much they want to bet
* The bet must be between `1` and the current money
* The user can choose to quit the game
* Update the player’s money after each round

Winning rules:

* All 3 symbols different → player loses the bet
* 2 of a kind → player gets `bet * rate`
* 3 of a kind → player gets `bet * 777 * rate`

Spin examples:

* 🍒 🍋 ⭐ → all different → lose
* 💎 💎 🍋 → 2 of a kind → win `bet * 11`
* ⭐ ⭐ ⭐ → 3 of a kind → win `bet * 777 * 9`
* 🔔 🍒 🔔 → 2 of a kind → win `bet * 7`

Important:

* The correct `rate` depends on the matching symbol
* Example: 3 × 🍋 → use rate `3`
* Example: 2 × 💎 → use rate `11`

Game ends when:

* The player chooses to quit
* OR the player runs out of money

Hints:

* Use `random.choice` or `random.randint`
* Keep track of symbol indexes to match the correct rate
* First check for 3 matches, then for 2 matches

## Question 3 – N-th Biggest Number

Write a function that gets:

* A list of numbers (with duplicates)
* A number `n`

The function should return the **n-th biggest unique number** in the list

Example:

`[88, 100, 90, 95, 95, 97, 97, 99, 97, 99] , n = 4`

Result:

`95`

Explanation:

Unique sorted values (descending):

`100, 99, 97, 95, 90, 88`

The 4th biggest number is `95`

Rules:

* Ignore duplicates when counting
* Assume `n` is valid (you don’t need to handle errors)

Hints:

* You can remove duplicates using a set
* Then sort the numbers
* Access the correct index

Good luck

Submission email: *[pythonai211225+python19prep@gmail.com](mailto:pythonai211225+python19prep@gmail.com)*
