# Connect 4: Adversarial Search & AI Agents

An exploration of Artificial Intelligence techniques applied to the classic game of Connect 4. This project implements and compares various adversarial search algorithms, ranging from basic heuristics to advanced Monte Carlo simulations, to create intelligent game-playing agents.

# Project Overview

The goal of this project was to develop a robust game engine and a suite of AI agents capable of playing Connect 4 at different levels of difficulty. The project focuses on:

State-Space Search: Navigating the game tree to find optimal moves.

Heuristic Design: Creating evaluation functions to estimate board strength.

Efficiency: Using pruning techniques to search deeper within time constraints.

Probabilistic Modeling: Using random playouts to determine positional advantages.

### Individual Project Note

This repository represents my individual work on implementing adversarial search strategies and analyzing their performance in a competitive environment.

# Key AI Agents

### Minimax Agent

Implements the classic Minimax algorithm for perfect information games. It assumes the opponent plays optimally and seeks to maximize the agent's guaranteed score.

### Alpha-Beta Pruning Agent

An optimized version of Minimax that significantly reduces the number of nodes evaluated in the search tree. This allows the AI to *look ahead* more turns without increasing computation time.

### Heuristic Agent

Uses a custom evaluation function to score non-terminal board states. It prioritizes creating *threes-in-a-row* and controlling the center of the board.

### Monte Carlo Simulation Agent

Instead of a deep tree search, this agent runs hundreds of random *playouts* for each possible move. It selects the column with the highest statistical win rate, proving effective even without complex heuristics.

# Key Technical Highlights

### Dynamic Board Representation

Implemented a flexible grid system (default 7x6) that handles gravity-based piece placement and efficient win-condition checking (horizontal, vertical, and diagonal).

### Search Tree Optimization

Utilized Alpha-Beta pruning to discard sub-optimal branches early, effectively doubling the search depth compared to standard Minimax.

### Center-Control Strategy

Statistical analysis within the project demonstrated that controlling the center column (Column 3) offers the most paths to victory, a strategy prioritized by the heuristic agents.

### Statistical Playout Analysis

Used Monte Carlo methods with **200**+ simulations per move to ensure statistical significance, allowing the agent to find strong positional moves in a 4 X 4 or 7 X 6 grid.

# Tech Stack

## Language

Python 3.x

## Libraries

NumPy: For efficient board state manipulation and matrix operations.

Math/Random: For simulation-based playouts and heuristic calculations.

Jupyter Notebook: For experimental results and algorithm visualization.

# Experimental Results

### Playout Win Rates

The Monte Carlo agent was tested by simulating games from different starting positions. Results confirmed that starting in the center increases the probability of winning by approximately 15-20% against a random opponent.

### Depth vs. Performance

Experiments showed a clear *intelligence* jump when moving from a depth-2 search to a depth-4 search, though the computational cost increased exponentially until Alpha-Beta pruning was applied.

# Project Limitations

### Lookahead Constraints

Without further optimizations like Transposition Tables, the search depth is limited by Python's execution speed for real-time play.

### Random Opponent Assumption

The Monte Carlo implementation assumes the opponent plays randomly during playouts, which can lead to over-optimism against a perfect-play Minimax agent.

# Setup and Installation

## Prerequisites

Python 3.9+

NumPy

## Installation

### Clone the repository

https://github.com/Avantiikaa16/connect4-ai-adversarial-search 

cd connect4-ai

### Install dependencies

pip install numpy

## Running the Experiments

Open the Jupyter Notebook to see the step-by-step implementation and results:

jupyter notebook assignment_connect4.ipynb

# Author

Avantika Ramesh Chapegadikar