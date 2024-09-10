# solveWordleCode
This project contains an alogorithm to solve the NYT Daily Wordle. 

**How To Use:**
1. Download the full_wordlist.txt file. This file contains a full list of potential words that are the answers for the wordle. The word list is taken from here. --> https://gist.github.com/cfreshman/d5fb56316158a1575898bba1eed3b5da
2. Download the appropriate version of the Chromedriver from here. --> https://googlechromelabs.github.io/chrome-for-testing/
3. Download the Python notebook.
4. install selenium if not installed
5. Run the Python notebook. ( I would recommend running each line individually and  waiting for visual confirmation from the visual confirmation from the wordle website)

**Limitations of the code**
1. It relies on a huge word list. It has all the valid words, however may contain words that may never be chosen as the wordle answer by NYT. In other words (no pun intended), it has words that may not be needed.
2. The algorithm picks the words randomly. There may be better ways of picking the words from the filtered lists other than random. For example, creating a probabilistic distribution to identify a word highly likely to be an answer. I may try doing that in future versions.
3. Because of the above limitation, the number of steps it takes to solve a wordle may vary a lot. I will try to make the code more efficient
4. The code does not automate logging in to your Wordle profile.

**High-level explanation of the algorithm **
1. The code installs and Imports the required Python libraries
2. It locates the chromeDriver and opens the website. Navigates to the window which takes wordle inputs
3. It identifies the letters that appear the most frequently
4. Creates a set of starter words, that are made of the most frequently used words
5. Pick a starter word randomly and put it in the wordle
6. Defines a function for filtering the words based on the feedback and hints from the first word.
7. Scrapes the hints from the website, sorts the letters according to the hints, and uses the function to filter a new set of words that meet the hint conditions.
8. Picks a word randomly from the list and tries in the wordle again
9. Repeat from step 7 till the correct word is found.
 
