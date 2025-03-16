# Escape the Castle - Reinforcement Learning Project

## Results & Analysis
The trained agent learned effective strategies for:
- Navigating the grid efficiently to reach the goal
- Making intelligent decisions when encountering guards
- Preserving health resources throughout the journey
- MBMC.py - trained with 1000000 episodes yielded values of [0.20942281 0.40589427 0.11007843 0.30892457]
- MFMC.py - trained with 1000000 episodes then played 100000 episodes using Q-table Averaged 8669.4373 , Assignment Expected >= 8600.

## Tools & Technologies Used
- **Python**
- **NumPy**:  Numerical operations for reinforcement learning algorithms
- **Gym Environment**: Custom environment based on OpenAI Gym for standardized RL interfaces
- **PyGame**: Optional visualization of the game environment and agent behavior
- **Pickle**: Serialization for storing trained Q-tables

## Key Reinforcement Learning Concepts Applied
- **Markov Decision Processes**: Foundation for the environment dynamics
- **Monte Carlo Methods**: Estimation through sampling and experience
- **Q-Learning**: Value-based reinforcement learning approach
- **Exploration vs. Exploitation**: Epsilon-greedy policy
- **Learning Rate Decay**: Adjust learning rates
- **Discount Factor** gamma

## Project Overview

In this project I implemented a Reinforcement Learning Algorithm to create a capable agent that navigagtes a virtual castle (represented as 5x5 grid). Agent **must** learn optimal 
strategies to escape the castle by reaching bottom right cell while avoiding/defeating guards randomly but strategically placed throughout the environment.

## Problem Statement
The challenge involves training an agent to:
1. Navigate from the starting position (0,0) to the goal position (4,4) (with out hardcoding of course)
2. Make optimal decisions when encountering guards (hide or fight) based off of health.
3. Learn the environment dynamic through **exploration and exploitation**

The environment is made with a Markov Decision Process (MDP) with probabilistic movement outcomes and guard interactions, making it a **complex decision problem**.

## Environment Details

### Grid Layout
- 5x5 grid with cells numbered from (0,0) to (4,4)
- Player starts in the top-left corner (0,0)
- Goal is located in the bottom-right corner (4,4)
- Four guards randomly positioned across the grid at the start of each game

### Player State
- **Position**: Current cell -  coordinates on the 5x5 grid
- **Health**: Three states - Full, Injured, Critical
- **Guard information**: What guard is in the cell with you

### Available Actions
- **Movement**: UP, DOWN, LEFT, RIGHT (90% success rate, 10% "slip" to random adjacent cell)
- **Interaction**: HIDE, FIGHT (only valid when in a cell with a guard else continues moving)

### Guard Interactions
- Guards have hidden (to the player/Agent) strength (affecting combat) and keenness (affecting hiding detection)
- Player must choose to hide or fight when encountering a guard
- Combat outcomes affect player health and position
- Failed hiding attempts force the player into combat

### Rewards & Penalties
- Reaching goal: +10,000
- Winning a fight: +10
- Losing a fight: -1,000
- Game defeat: -1,000 

## Approaches Implemented

### 1. Model-Based Monte Carlo (MBMC) MBMC.py file
I implemented a Model-Based Monte Carlo approach to estimate the probability of victory against each guard in the castle. This approach:

- Executes random actions to gather data from the environment
- Tracks encounters with each guard and fight outcomes (encounters, wins, => win probability)
- Calculates win probabilities for each guard based on interactions
- Returns a numpy array of amount of guards-length with probabilities with beating each guard

Key implementation aspects:
- Random exploration of the environment
- Data collection and analysis
- No prior assumptions about guard attributes
- No outside information accessed about game/environment except Agent Position, Current Health, which Guard in your cell?, and game score

Utility: 
Returns a numpy array [0. 0. 0. 0.] with estimated battle/win probabilities for Guards 1-4

### 2. Model-Free Monte Carlo (MFMC) with Q-Learning
I developed a Q-learning agent that learns the value of state-action pairs through direct interaction with the environment. This approach:

- Maintains and updates a Q-table containing estimated reward values for state-action pairs
- Maintains and updates an UpdatesTable containing frequency of move for state-action pairs
- Uses an epsilon-greedy policy for balancing exploration and exploitation
- Applies dynamic decaying learning rates 
- Incorporates experience replay to improve efficiency

Key implementation aspects:
- Q-table State representation through a hash function (mapping to integers 0-375)
- updatesTable representation through a hash function (as well mapping from 0 - 375)  
- Decaying exploration rate to transition from exploration to exploitation
- Bellman equation updates to information in Q-table
- Progress tracking through terminal

The Model-Based Monte Carlo approach provided valuable insights about guard strengths, while the Q-learning agent developed a comprehensive policy for navigating the environment optimally.
