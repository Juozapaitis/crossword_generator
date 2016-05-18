Crossword Generator
===

This very simple Python script generates a *clueless* crossword puzzle. It harnesses the capabilities of Python and LaTeX to output the puzzle in a printable PDF.

Algorithm
---

I purposefully designed and implemented this little project without performing research on crossword generation techniques; I wanted to see if I could do it by myself. The very simple algorithm that is implemented here is as follows:

1. The technique receives a list of words, in a .txt file (I tested using [these](http://www.gwicks.net/dictionaries.htm) lists).
2. A number (100, by default) of words are chosen randomly from the list that is given, and these are the words that will be used hereafter.
3. The technique expands the list of words into a list of possibilities, where each possibility encodes a possible starting location for a word, as well as its direction. This essentially constitutes all possible words that can be placed into the grid.
4. A new word is taken from the list of possibilities and placed on the grid. This makes it so a number of possibilities are now invalid, and these are removed from the list. Steps 3 and 4 are repeated until the grid is as full as we want it to be.