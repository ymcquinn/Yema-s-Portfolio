# Wumpus World — POMDP Analysis

Empirical analysis of a partially observable RL environment to identify failure modes and design fixes.

## Problem

Wumpus World is a classic RL benchmark: an agent navigates a grid, avoids pits, shoots the Wumpus, grabs gold, and exits. The agent receives a 5-dim percept `[stench, breeze, glitter, bump, scream]` — but the percept is not a state.

## Findings

- **Percept aliasing is real and severe.** Empirically demonstrated that one percept maps to 9+ distinct world states, breaking the Markov property.
- **Random policy fails badly.** Averaged −354 reward across 50 episodes vs. −1 for a trivial "always exit immediately" policy.
- **Curriculum learning is necessary.** Without it, any RL agent converges to the always-exit policy because −1 dominates every other baseline.

## Proposed solution

Belief-state tracking — a probability distribution over possible world states given the history of actions and percepts — restores the Markov property. This converts the POMDP into a belief-MDP.

## Stack
Python · custom environment
