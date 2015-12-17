# How to use this repo
    Fork the repo 
    create a branch off of master with your github/name handle
    commit and push to your repo/branch
    send pull request for your handle branch 

    With all solutions in one place, you can come back and look at each other's code

# Toy problem solving guidelines/ tips

    1. Make note of the input and outputs required by the problem. 

      Example 1: Sudoku solver - input in form of string with line breaks that restricts what you can do on the input unless you change it/ transform it
      Example 2: Military Time - both input and output are strings. But, might have to think about converting to integers for doing math.


    2. Take or create a small test case and solve it by hand without any programming logic
      Example: Telephone Words - create all permutations by hand. 


    3. What data types to use
      After you have a manual solution, to start thinking about code representation, start with data types.
      
      Think about use of Arrays vs Objects vs Strings
        
        JavaScript strings are immutable, while arrays are quite mutable
        Many array methods modify in place while the same string method would create and return a new string
        You can borrow Array methods by applying (call/apply) the Array prototype methods 
        (Ex: Array.prototype.arrayMethod.call(,) )
        Only non mutating array methods can be borrwed by strings (Ex: join, map)
 
        For using array mutators, convert to array, operate and then convert back to string (Ex: reverse)

        Objects are great for storing information when you want the collection elements to be unique ( can force keys to not be overwritten or overwritten as required)

        Go to MDN and learn more inbuilt functions for various data types, it will help you approach the toy problems in more ways.

        Some basic functions: slice, splice, reverse, indexOf, concat, toString, parseInt, each
        Some advanced functions: map, reduce, filter, indexOf, ...


    4. Transformations and Manipulation of data 
      Think about what you might need to do to the given data to get to your solution
      This might require you to change the data type you chose to store your intermediate values in


    5. Algorithm
      First write in plain english the steps you are going to follow.
      Then Psuedocode the solution. Maintain nesting and indentation in your psuedocode like you would in code.


      Example: Sum Array - solving by hand a small example is easy but problem becomes more challenging when trying to represent in code. In this case you have to answer the following questions:


# 1 - JS basics and working with data types
    Problem Description:

    The word i18n is a common abbreviation of internationalization the developer community use instead of typing the whole word and trying to spell it correctly. Similarly, a11y is an abbreviation of accessibility.

    Write a function that takes a string and turns any and all words within that string of length 4 or greater into an abbreviation following the same rules.

    Note:

    A "word" is a sequence of alphabetical characters. By this definition, any other character like a space or hyphen (eg. "elephant-ride") will split up a series of letters into two words (eg. "elephant" and "ride").
    The abbreviated version of the word should have the first letter, then the number of removed characters, then the last letter (eg. "e6t-r2e").



# 2 - nested loop logic
    Write a function x(n) that takes in a number n and returns an nxn array with an X in the middle. The X will be represented by 1's and the rest will be 0's. 
    E.g.

    x(5) === [[1, 0, 0, 0, 1],
              [0, 1, 0, 1, 0],
              [0, 0, 1, 0, 0],
              [0, 1, 0, 1, 0],
              [1, 0, 0, 0, 1]];

    x(6) === [[1, 0, 0, 0, 0, 1],
              [0, 1, 0, 0, 1, 0],
              [0, 0, 1, 1, 0, 0],
              [0, 0, 1, 1, 0, 0],
              [0, 1, 0, 0, 1, 0],
              [1, 0, 0, 0, 0, 1]];


# 3 - puzzles and algorithms 
    There are 8 balls numbered from 0 to 7. Seven of them have the same weight. One is heavier. Your task is to find it's number.

    Your function findBall will receive single argument - scales object. The scales object contains an internally stored array of 8 elements (indexes 0-7), each having the same value except one, which is greater. It also has a public method named getWeight(left, right) which takes two arrays of indexes and returns -1, 0, or 1 based on the accumulation of the values found at the indexes passed are heavier, equal, or lighter.

    getWeight returns:

    -1 if left pan is heavier

    1 if right pan is heavier

    0 if both pans weight the same

    Examples of scales.getWeight() usage:

    scales.getWeight([3], [7]) returns -1 if ball 3 is heavier than ball 7, 1 if ball 7 is heavier, or 0 i these balls have the same weight.

    scales.getWeight([3, 4], [5, 2]) returns -1 if weight of balls 3 and 4 is heavier than weight of balls 5 and 2 etc.

    So where's the catch, you may ask. Well - the scales is very old. You can use it only 4 TIMES before the scale breaks.


    Next level:
    You can use it only 3 TIMES before the scale breaks.

    Extra credit:
    You can use it only TWICE before the scale breaks.


# 4 - code challenge
    Your task is to write a function for calculating the score of a 10 pin bowling game. The input for the function is a list of pins knocked down per roll for one player. Output is the player's total score.

    Rules of bowling in a nutshell:

    A game consists of 10 frames. In each frame the player rolls 1 or 2 balls, except for the 10th frame, where the player rolls 2 or 3 balls.
    The total score is the sum of your scores for the 10 frames
    If you knock down fewer than 10 pins with 2 balls, your frame score is the number of pins knocked down
    If you knock down all 10 pins with 2 balls (spare), you score the amount of pins knocked down plus a bonus - amount of pins knocked down with the next ball
    If you knock down all 10 pins with 1 ball (strike), you score the amount of pins knocked down plus a bonus - amount of pins knocked down with the next 2 balls
    Rules for 10th frame

    As the 10th frame is the last one, in case of spare or strike there will be no next balls for the bonus. To account for that:

    if the last frame is a spare, player rolls 1 bonus ball.
    if the last frame is a strike, player rolls 2 bonus balls.
    These bonus balls on 10th frame are only counted as a bonus to the respective spare or strike.

    Extra credit: interview level task
    Make an api that does the above that allows a client to plug in and play
    Also make a sample front-end to test your game


