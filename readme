# Agent for Bluffing Card Game

This project is an agent designed to play and win a bluffing-style card game against a human opponent. The agent's core objective is to learn the user's unique playing patterns and tendencies over multiple rounds to improve its strategy.

The agent operates in what is known as a Partially Observable Stochastic Environment (POMDP), meaning it cannot see the user's cards (the state) but can observe their actions (what they play).

## Agent Behavior

The model is designed to be an adaptive, learning opponent:

* **Adaptive Learning:** The agent's player profile is persistent across rounds. It is designed to learn and build a profile of its opponent as they play multiple games.
* **Dynamic Challenging (Explore vs. Exploit):** In the early stages of a game, the model will challenge the user more often. This is an "exploration" phase to gather data and build an internal model of the user's honesty. As the game progresses and the model's confidence in its belief state grows, it will challenge less and "exploit" its learned knowledge.
* **Belief State Maintenance:** The core of the agent is its internal belief state. This is a model of what cards the agent *thinks* the user currently holds. This state is updated after every move the user makes.

##  Technical Approach: Belief-Based RL

This project uses a **Belief-Based Reinforcement Learning** framework. Because the agent cannot see the user's cards, it cannot act on the "true" state of the world. Instead, it acts based on its *belief* of the state.

### Internal Belief State

The agent's internal belief state, which informs all its decisions, is comprised of several key factors:

* **Game Context:** How many cards the player has left. (e.g., a user's behavior may change dramatically when they only have one card left).
* **Game Outcomes & Ratios:** A running tally of the user's observed behavior (e.g., "How many times have they lied vs. how many times have they been honest?").
* **Response Timings:** How quickly or slowly the user makes a move, which can be a correlated signal for bluffing.
* **Mental Model of User's Cards:** The agent's probabilistic estimate of the cards remaining in the user's hand.

## Project Scope

### In Scope
* Playing multiple rounds with a single user.
* Creating an ML model that learns the user's specific patterns over time.
* Using the learned patterns to defeat the user.

### Out of Scope
* Adding visual inputs (e.g., using a camera to read a user's facial expressions).