# 🪨📄✂️ TorchRPS

A Rock Paper Scissors game powered by a PyTorch neural network that learns to predict and counter your moves.

---

## Overview

TorchRPS combines a playable Rock Paper Scissors game (built with Pygame) with a neural network AI opponent that trains on your move history in real time. The more you play, the smarter it gets — learning your patterns and tendencies to try to beat you.

## Features

- **Neural network AI** built with PyTorch that adapts to your playstyle
- **Pygame-powered game interface** for smooth, interactive gameplay
- **Real-time training** — the model updates as you play
- **Training visualization** via Matplotlib to track model performance over time
- **Modular project structure** separating AI logic, game code, and utility scripts

## Project Structure

```
TorchRPS/
├── ai/          # Neural network model, training logic, and prediction
├── game/        # Pygame game loop, rendering, and input handling
├── scripts/     # Utility scripts (e.g. training runs, data export)
├── requirements.txt
└── README.md
```

## Requirements

- Python 3.10+
- PyTorch 2.2.0
- Pygame 2.5.2
- NumPy 1.26.4
- Matplotlib 3.8.2

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/ZaneColeRileyDev/TorchRPS.git
   cd TorchRPS
   ```

2. **Create and activate a virtual environment** (recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## Usage

Launch the game:
```bash
python game/main.py
```

To run a standalone training script:
```bash
python scripts/train.py
```

## How It Works

The AI uses a feedforward neural network trained on a sliding window of your previous moves. It learns to recognize patterns in your choices (e.g. favoring Rock after a loss) and selects the move that would beat your predicted next choice. The model is trained incrementally using backpropagation after each round, so it continuously improves throughout a session.

## Tech Stack

| Library | Purpose |
|---|---|
| PyTorch | Neural network definition and training |
| Pygame | Game window, rendering, and input |
| NumPy | Move encoding and data handling |
| Matplotlib | Training loss and accuracy plots |

## License

MIT — see [LICENSE](LICENSE) for details.
