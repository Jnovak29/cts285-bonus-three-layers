# NOTES: Three Layers

Your name: TODO

Fill each TODO. Write plain, short sentences. Do not delete the headings.

## Part 1. Predict, then find [S1]

Write your prediction before you open any code. Then search. In the last column, write each file the search finds and what that file does.

| Action | Search word | My prediction (file) | Files found and what each does |
|---|---|---|---|
| Prints "Not yet. Try again." | `Not yet` | app.py | Found the app.py file, it is part of the user interface code and is a feedback message.  |
| Decides that the second miss shows the answer | `reveal` | check.py | Found in the app.py and is part of the business logic handling, displays the hidden number after second attempt |
| Saves one attempt | `save_attempt` | store.py | This file calls save_attempt() whenever an answer is submitted |
| Refuses the 11th problem | `SetFull` | bank.py | This defines the exception and contains the class that is responsible for preventing the 11th problem from being stored |

Search command: `grep -rn "SEARCH WORD" --include=*.py .`

## Part 2. What the program remembered [S1]

After the restart, what did the program remember? The attempt that I stopped at.

Which file made that possible? The Json File is what saved the data.

## Part 3. The interface change [S1]

What did you change in `app.py`? Changed the "try again" output when answer is wrong to another output.

Why did no test need to change? Tests did not have to change becuase the changed code was in the user interface and had no affect on logic or behavior.

## Part 4. The rule in the real library [S2]

The same 10-problem rule exists in the real library. Write the file and the function name. 
File: dataman/bank.py
Function add_problem()

## Part 5. The red test [S2]

With the rule removed from the library, what did the screen show?
it failed a pytest

With the rule removed, which test failed? 
test/test_logic.py::test_eleventh_problem_is_refused



## Part 6. The data swap [S2]

A real database would replace which file?
The Json file dataman_store.json

Which file holds the rules and does not change when the database changes? 
The Business Logic - logic.py

## Reflection [S2]

Write 3 to 5 sentences. Pick one layer. Say what you changed in it. Say what stayed the same in the other two layers.
I modified the interface layer by changing the message shown when the user enters a incorrect answer. the only thing that was was affected is what the user sees
displayed by the code. the logic later and data layer stayed the same.

## Beta feedback (optional)

This bonus is a beta test. Which step took longer than its time? What confused you? Write it here. Your answer helps the next class.
