# Kitchen Stock Assignment

A small Python exercise from freeCodeCamp's Python course, on functions, variables and variable scope.

## What the program does

- Stores the quantities of eggs, flour and sugar in variables.
- `check_kitchen_stock()` prints the stock and a total.
- `use_eggs()` checks whether there are enough eggs, prints a message, and returns the remaining quantity.
- `make_fried_egg()` uses `use_eggs()` and prints whether a fried egg could be made.

## How to run

Run `python main.py` (Python 3).

Expected output:

```text
The kitchen has 6 total items:
- 1 eggs
- 2 flour
- 3 sugar
1 egg(s) used out of 1 available.
1
1 egg(s) used out of 1 available.
Made a fried egg. Yummy!
```

## What this exercise shows

- A function parameter can share a name with a global variable, but it is a separate local variable inside the function.
- The first call to `use_eggs()` does not change the global `available_eggs`, because its returned value is not assigned. That is why `print(available_eggs)` shows 1.
- `make_fried_egg()` returns the new egg count, and assigning the result back changes the global value to 0.

## Limitations and ideas

- The total adds quantities of different ingredients (eggs, flour and sugar), so it is a count of units, not of distinct items.
- Possible next step: store the stock in a dictionary and check a recipe's ingredients against it. This is the starting point for a broader workflow tool idea.
