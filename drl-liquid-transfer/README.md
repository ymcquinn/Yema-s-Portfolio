# Autonomous Liquid Transfer — Deep RL Environment

A MuJoCo-based reinforcement learning environment simulating a robotic pipette arm performing beaker-to-petri-dish liquid transfer.

## Why this project

Autonomous liquid handling is the throughput floor for self-driving labs — the minimum reliable capability a robot needs before it can be trusted with real experiments. This environment is the first step toward an SDL pipeline for optimizing *Cordyceps militaris* fermentation conditions to maximize cordycepin yield.

## Environment

| Component | Specification |
|---|---|
| Simulator | MuJoCo |
| Robot | 3-DOF arm + 9-DOF three-finger hand (12 actuators) |
| Workspace | 1m × 1m table with randomized container positions |
| Observation space | 70-dim vector — object-centric vision, proprioception, motor resistance, fluid state |
| Action space | 12 continuous joint position targets |
| Reward | Proximity + aspiration + dispensing + success + grasp-force penalty |
| Curriculum | Static → randomized targets → disturbances |

## Design decisions

- **Position actuators over torque** — initial torque control was numerically unstable (tiny finger joints → NaN within 2 timesteps). Switched to PD position control, matching Robosuite and MuJoCo Menagerie conventions.
- **Object-centric observation over pixels** — faster training, standard for MuJoCo manipulation tasks, and matches the actual deployment target (fixed overhead camera in a lab).
- **Abstracted fluid state** — the goal is training the agent, not simulating fluid mechanics. Volumes are tracked as scalar state, matching industry SDL platforms.

## Status

- ✅ Environment implemented and verified
- 🔄 PPO training (Stable-Baselines3)
- ⏳ Evaluation metrics + curriculum validation

## Run

```bash
pip install mujoco gymnasium numpy
mjpython advanced_transfer_env.py    # macOS
python advanced_transfer_env.py      # Windows/Linux
