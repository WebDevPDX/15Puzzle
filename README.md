# 15 Puzzle

##Project Outline

* Create a simple 15 sliding puzzle
* total time alotted: ~ 4 hours

##Why I did what I did

* At first I wanted to go with a 2 dimensional array like I normally would for this kind of grid setup but then I reconsidered that I don't need the same functionality of rows / cols if I bind bind the content of the cell and pass it on click. That way I am saving processing time as no stacked loops are necessary for move checks
* I decided instead of checking where the 'null' cell is that I can simply run a check based on the clicked cell when it is clicked. As there are only 4 possible directions it makes the check very easy and the I can go with a simple if / then logic checking array position -4 (above), -1 (left), +1 (right) and +4 (below). This again saves looping through arrays. 
* There is a challenge with these puzzles as only about 50% of them are solvable. Since I did not want to give my players unsolvable puzzles I implemented the boardcheck() which checks the solvability of the generated gameField. You can read more here: https://en.wikipedia.org/wiki/15_puzzle
* I implemented win check as a very simplistic function comparing using a sorted comparison array and stringifying both gameField and comparisonArr as this will yield the result I am looking for and again no loops are necessary
* I finally decided to style it simiarly to the 15 puzzle I played as a kid with a big red plastic frame and inset sliding tiles

##Possible Impovements
* generate different levels where players have to sort color coded tiles instead of numbers. Display the expected result next to it
* replace the numbers with images and have a player sort the images snippets into a whole picture
* create a DB. Stringify the starting gameField and save it with the number of moves a player needed. Display the top 10 players for each configuration next to the gameField
