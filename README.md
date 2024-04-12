Unit test specifications should take the form of:
Expect [action] to be [some result]

Functional test specifications can be worded slightly more naturally:
When a user [does something with some parameters], [some thing should happen]

Prompts:
For each prompt below:
1. Read the prompt
2. Identify the expectations
3. Write specifications in pseudocode/plain English for all the tests that would be useful for that prompt
    a. try to take any "edge cases," or unexpected circumstances, into account, and write test specs for them
    b. try not to write extraneous tests

Unit Tests:
1. A function called "multiplication" that returns the product of the two input numbers.
    Expect multiplication(x, y) to be a number
    Expect multiplication(3, 2) to be 6
    Expect multiplication("x", 2) to be an error
    Expect multiplication( , ) to be undefined

2. A function called "concatOdds" takes two arrays of integers as argunments. It should return a single array that only contains the odd number, in ascending order, from both arrays.
    Expect concatOdds([3, 2, 1], [4, 5, 6]) to be concatenated
    Expect concatOdds([3, 2, 1], [4, 5, 6]) to be filtered
    Expect concatOdds([3, 2, 1], [4, 5, 6]) to be arranged in asceding order
    Expect concatOdds([2, 4, 6], [8, 10, 10]) to be undefined
    Expect concatOdds([1, 1, 3], [3, 5, 5]) to be [1, 3, 5]
    ??Expect concatOdds(["a", 2, 1], [4, 5, 6]) to be [1, 5]??
    Expect concatOdds([3, 2, 1], [4, 5, 6]) to be an array



Functional Tests:
1. A shopping cart checkout feature that allows a user to check out as a guest (without an account), or as a logged-in user. They should be allowed to do either, but should be asked if they want to create an account or log in if they check out as a guest.
    When a guest user clicks on shopping cart, ask if they want to continue as guest or log in as user
    When a user clicks on shopping cart, proceed to checkout and autofill user information
    When a guest user clicks log in as user, ask to enter information or click to create an account
    When a guest user clicks continue as guest, proceed to checkout
    When a user proceeds to check out, ask for delivery, payment and billing information 
    When a guest user enters information at checkout, ask if they'd like to save information for faster checkout in future
    When a guest user clicks save information for faster checkout in future, prompt guest user to create account to save information
    When user proceeds to checkout with empty shopping cart, prompt them that the cart is empty and ask to return to shopping page
    When checkout is completed, move user to a "thank you" page
