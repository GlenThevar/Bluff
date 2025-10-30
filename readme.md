# Bluffing Card Game Agent

## Overview

This project is an agent designed to play and win a bluffing-style card game against a human opponent. The agent's primary goal is to adapt and learn the opponent's unique playing patterns over multiple rounds to improve its strategic decisions.

The agent operates within a **Partially Observable Stochastic Environment (POMDP)**. It cannot directly observe the opponent's cards but can track and analyze the actions the opponent takes (i.e., the cards they play).

## Features

### Agent Behavior

The agent is designed to be an adaptive opponent that learns and adjusts its strategy throughout the game:

- **Adaptive Learning**: The agent maintains a persistent player profile across rounds, learning and evolving based on the user's behaviors and tendencies.
  
- **Dynamic Challenge Strategy (Explore vs. Exploit)**: 
  - **Exploration Phase**: In the early stages of the game, the agent challenges the user more frequently to gather data and form an understanding of the user's strategy and bluffing behavior.
  - **Exploitation Phase**: As the agent gains confidence in its beliefs about the opponent's patterns, it shifts to an exploitative strategy, using the learned information to make more informed decisions and reduce challenges.

- **Belief State Maintenance**: The agent’s internal belief state continuously updates as the game progresses. This belief state serves as the foundation for decision-making, helping the agent predict the user's behavior and react accordingly.

## Technical Approach

### Belief-Based Reinforcement Learning (RL)

This agent leverages a **Belief-Based Reinforcement Learning (RL)** framework. Since the agent cannot access the true state of the game (i.e., the opponent's cards), it relies on its belief state, which is based on observed actions rather than the actual game state.

### Internal Belief State

The internal belief state plays a crucial role in guiding the agent’s decisions. It is formed based on several factors:

- **Game Context**: The agent tracks the number of cards remaining in the user’s hand, as player behavior may vary when they have fewer cards left.
  
- **Game Outcomes & Ratios**: The agent keeps a running tally of the user’s actions (e.g., how often they bluff or tell the truth) to detect patterns over time.

- **Response Timings**: The timing of the user’s moves may provide indirect clues about their strategy. Faster moves may indicate confidence, while slower moves could suggest hesitation or bluffing.

- **Mental Model of the User's Cards**: Based on observed moves, the agent probabilistically estimates which cards the opponent likely holds.

## Project Scope

### In Scope

- **Multiple Game Rounds**: The agent plays multiple rounds with a single user to build and refine its understanding of the opponent's behavior.
- **Machine Learning Model**: The agent employs machine learning to learn and adapt to the user’s specific playstyle over time.
- **Opponent Defeat**: The agent utilizes its learned patterns and strategies to challenge and ultimately defeat the user.

### Out of Scope

- **Visual Inputs**: The project does not include using external sensors, such as cameras, to analyze the user’s facial expressions or physical cues.
