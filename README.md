# Snake AI with Deep Q-Learning

This project implements an AI agent that learns to play the classic Snake game using Deep Q-Learning with PyTorch.

## Model Description

The AI uses a simple neural network with two fully connected layers:

- **Input layer:** 11 features representing the current game state, including danger directions, current movement direction, and food location relative to the snake's head.
- **Hidden layer:** 256 neurons with ReLU activation.
- **Output layer:** 3 outputs representing possible actions — move straight, turn right, or turn left.

The model learns by interacting with the game environment, receiving rewards for eating food (+10), penalties for collisions (-10), and training its Q-values accordingly.

---

## Project Structure

- `agent.py` - Contains the AI agent implementation and training loop.
- `game.py` - Contains the Snake game logic using Pygame.
- `model.py` - Defines the neural network model and trainer classes using PyTorch.
- `helper.py` - Utility functions, including plotting training progress.

---

## Requirements

To run this project, you need Python 3.7 or higher.

Required Python packages:

- pygame
- numpy
- torch
- matplotlib
- ipython (for interactive plotting)

You can install all dependencies using:

```bash
pip install -r requirements.txt
```
---

## Run the Application

To start training the AI to play Snake, run the following command in your terminal:

```bash
python agent.py
```