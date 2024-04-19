# Minesweeper

This code implements a basic AI for the game of Minesweeper. The AI uses a knowledge-based agent approach, which is a type of AI that uses a knowledge base of information and inference procedures to make decisions.

## minesweeper.py

The code is divided into three main classes: Minesweeper, Sentence, and MinesweeperAI.

Minesweeper: This class represents the game itself. It initializes the game board with a specified height, width, and number of mines. It also includes methods for printing the board, checking if a cell is a mine, counting nearby mines, and checking if all mines have been found.

Sentence: This class represents a logical statement about the game. A sentence consists of a set of board cells and a count of the number of those cells which are mines. It includes methods for identifying known mines and safe cells, and for updating the sentence when a cell is known to be a mine or safe.

MinesweeperAI: This class represents the AI player. It keeps track of moves made, known safe cells and mines, and a knowledge base of sentences about the game. It includes methods for marking a cell as a mine or safe, adding new knowledge based on a safe cell and the count of neighboring mines, making a safe move, and making a random move.

## The AI

The AI uses a simple inference-based approach to decide its next move. When it learns the number of mines adjacent to a safe cell, it adds a new sentence to its knowledge base. It then updates its knowledge base to mark any additional cells as safe or mines if it can be concluded from the sentences in the knowledge base. If it can't make a definite safe move, it makes a random move.

This AI does not guarantee a win every time, as Minesweeper is a game that can require guesswork in certain situations. However, it uses all the information it has available to make the safest possible moves.

## Run locally

Clone the repository to your local machine. Install the requirements and execute the runner.py file. A window will open where you can play the game yourself or let the AI choose the next move.