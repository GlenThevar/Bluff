# Bluffing Card Game Agent

## Overview

This project is an agent designed to play and win a bluffing-style card game against a human opponent. The agent's primary goal is to adapt and learn the opponent's unique playing patterns over multiple rounds to improve its strategic decisions.

The agent operates within a **Partially Observable Stochastic Environment (POMDP)**. It cannot directly observe the opponent's cards but can track and analyze the actions the opponent takes (i.e., the cards they play).

## Project Phase
#### Phase 1 – Basic CLI Game
**Goal:** Validate game rules and flow, Fully random (non-intelligent) agent

#### Phase 2 – Heuristic Agent
**Goal:** Introduce strategic play without learning, Probability estimates, Handcrafted strategies

#### Phase 3 – Belief State Design
**Goal:** Model uncertainty in a partially observable environment, Probabilistic representation of opponent hands, Bayesian updates after each action

#### Phase 4 – Belief-Based Heuristic Agent
**Goal:** Replace fixed assumptions with belief-driven decisions, Dynamic strategy adjustment

#### Phase 5 – Reinforcement Learning in a POMDP
**Goal:** Learn optimal strategies under partial observability, Game formalized as a POMDP

#### Phase 6 – Frontend Development
**Goal:** Improve usability and accessibility, User-facing interface

## Status
**Active Development** — features are implemented incrementally following the roadmap above.


