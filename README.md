# Kessler-Controller 
A fuzzy logic AI controller for the Kessler Game, a Python-based implementation of the classic Asteroids arcade game. This project was developed for ECE 449: Intelligent Systems Engineering at the University of Alberta.

The controller is designed to control a player ship in real time by making decisions for thrust, turning, firing, and mine deployment based on the current game state.

## Overview

The Kessler Game provides a simulation environment where controller agents compete by navigating an Asteroids-style game world. At every game step, the controller receives the current ship state and game state, then returns four control outputs:

* `thrust`: how much acceleration to apply in the ship’s current direction
* `turn_rate`: how quickly the ship should rotate
* `fire`: whether the ship should fire a bullet
* `drop_mine`: whether the ship should deploy a mine

This project implements a fuzzy-control-based agent that evaluates asteroid positions, ship state, targeting conditions, and movement decisions to choose actions during gameplay.

## Project Goals

The main goals of this project were to:

* Build an intelligent fuzzy logic controller for the Kessler Game
* Control all four required ship actions: thrust, turn rate, firing, and mine dropping
* Improve performance against the default test controller
* Use rule-based fuzzy inference to make interpretable gameplay decisions
* Experiment with controller tuning to improve survival, asteroid avoidance, and scoring

## Team Members

This project was completed as a group project for ECE 449: Intelligent Systems Engineering.

Team members:

* Tabish Khan
* Miles Taylor
* Amara Yu


## Technologies Used

* Python
* Kessler Game
* scikit-fuzzy
* NumPy
* Fuzzy logic control
* Game AI
* Real-time decision-making

## Repository Structure

```text
Kessler-Controller/
├── src/
│   └── controller implementation files
├── my_controller_v3.py
├── README.md
├── LICENSE
├── .gitignore
└── .gitmodules
```

## How It Works

The controller follows the Kessler Game controller interface. The core logic is implemented inside the `actions()` method, which is called once per game timestep.

At each timestep, the controller:

1. Reads the current ship state and game state
2. Identifies relevant asteroid threats
3. Computes targeting and movement information
4. Applies fuzzy logic rules to determine ship behavior
5. Returns thrust, turn rate, fire, and mine-drop decisions

The fuzzy controller allows the agent to make smooth, interpretable decisions instead of relying only on hard-coded thresholds.

## Key Features

* Real-time asteroid targeting
* Fuzzy turn-rate control
* Fuzzy firing decisions
* Thrust control for movement and positioning
* Mine deployment logic
* Controller tuning for improved game performance
* Branch-based development for individual contributions

## My Contribution

My work is available on the `tabish` branch of this repository.

I contributed to the controller implementation and tuning, including improvements to ship behavior, thrust handling, and fuzzy decision-making logic.

Branch link:

```text
https://github.com/Tak701/Kessler-Controller/tree/tabish
```

## Running the Project

To run the controller, install the Kessler Game environment and required Python dependencies, then run the game scenario file with this controller included.

General setup:

```bash
pip install kesslergame
pip install scikit-fuzzy numpy
```

Then configure the scenario file to import and use the controller.

Example:

```python
from my_controller_v3 import MyController
```

and include the controller in the game run configuration.

## Notes

This project was completed as part of a university course project. Some implementation details may reflect assignment requirements, testing constraints, or course-specific setup.

## License

This repository includes an Apache 2.0 license.
