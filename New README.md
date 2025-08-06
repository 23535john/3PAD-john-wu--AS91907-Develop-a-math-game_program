# 3PAD-john-wu--AS91907-Develop-a-math-game_program
Spongebob theme
# 🧽 SpongeBob Jellyfish Catcher: Math Adventure

![Game Screenshot](assets/Images/game_screenshot.png) *Example gameplay screen*

## Table of Contents
1. [Game Overview](#game-overview)
2. [Features](#-features)
3. [Installation](#-installation)
4. [How to Play](#-how-to-play)
5. [Game Structure](#-game-structure)
6. [Customization](#-customization)
7. [Troubleshooting](#-troubleshooting)
8. [Credits](#-credits)

## Game Overview
SpongeBob Jellyfish Catcher is an educational math game set in the vibrant world of Bikini Bottom. Players help SpongeBob catch jellyfish while solving math problems across three difficulty levels. The game combines math practice with engaging gameplay, colorful visuals, and SpongeBob-themed adventures.

## ⭐ Features
- **Three Unique Difficulty Levels** with themed environments:
  - 🐙 Jellyfish Fields (Easy)
  - 🦀 Krusty Krab (Medium)
  - 🎷 Squidward's House (Hard)
- **Interactive Jellyfish Mechanics** with physics-based movement
- **Comprehensive Math Problems** covering:
  - Basic arithmetic
  - Percentages and sequences
  - Equations and geometry
  - Problem-solving strategies
- **Player Progression System**:
  - Score tracking
  - Lives system
  - Question counter
- **Leaderboards** with player ranking
- **Mistake Review System** with detailed explanations
- **Audio System** with background music and sound effects
- **Responsive UI** with full-screen support

## 📥 Installation
### Requirements
- Python 3.8+
- Tkinter (usually included with Python)
- Pygame (for audio support)

### Installation Steps
1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/spongebob-math-adventure.git
   cd spongebob-math-adventure
   ```

2. **Install dependencies**:
   ```bash
   pip install pygame
   ```

3. **Run the game**:
   ```bash
   python main.py
   ```

## 🎮 How to Play

### Game Flow
1. **Main Menu** - Start new game, view leaderboards, or exit
2. **Player Setup** - Enter your name and select difficulty
3. **Gameplay** - Solve math problems by catching jellyfish
4. **Results** - View score, review mistakes, and see leaderboard position

### Controls
- **Mouse**: Click and hold jellyfish to select answers
- **Keyboard**: Not required - fully mouse-driven interface

### Game Mechanics
- **Scoring**:
  - Easy: 50 points per correct answer
  - Medium: 100 points per correct answer
  - Hard: 300 points per correct answer
- **Lives System**: Start with 3 lives, lose one for incorrect answers or timeouts
- **Timer**: 60 seconds per question
- **Questions**: 12 questions per game session

### Difficulty Levels
| Level | Location | Math Concepts | Points/Question |
|-------|----------|---------------|-----------------|
| Easy | Jellyfish Fields | Basic arithmetic, counting, money | 50 |
| Medium | Krusty Krab | Equations, percentages, sequences | 100 |
| Hard | Squidward's House | Quadratics, systems, geometry | 300 |

## 🧩 Game Structure

### File Structure
```
spongebob-math-adventure/
├── assets/                  # Game resources
│   ├── Images/              # Visual assets
│   └── Sounds/              # Audio files
├── game_objects.py          # Jellyfish, leaderboard, instructions
├── Game_core.py             # Main game pages and logic
├── main.py                  # Entry point
├── utils.py                 # Problem generator, score manager, audio
└── README.md                # This file
```

### Key Components
1. **MathAdventureGame Class** (main.py)
   - Manages game window and page navigation
   - Handles player data and game state

2. **ProblemGenerator Class** (utils.py)
   - Creates math problems based on difficulty
   - Generates answer options with distractors

3. **JellyfishManager Class** (game_objects.py)
   - Creates and animates jellyfish with physics
   - Manages answer bubble display

4. **ScoreManager Class** (utils.py)
   - Saves and loads high scores
   - Tracks player progress

5. **AudioManager Class** (utils.py)
   - Handles background music and sound effects
   - Provides music toggle functionality

## 🎨 Customization
You can modify these files to customize your game experience:

1. **Adjust Difficulty**:
   - Modify `QUESTIONS_PER_GAME` and `TIME_PER_QUESTION` in `Game_core.py`
   - Edit problem parameters in `utils.py` (ProblemGenerator class)

2. **Change Visuals**:
   - Replace images in `assets/Images/` (maintain same filenames)
   - Modify colors in `BACKGROUND_COLORS` dictionary in `Game_core.py`

3. **Modify Game Mechanics**:
   - Adjust jellyfish speed in `SPEEDS` dictionary in `game_objects.py`
   - Change scoring values in `LEVEL_POINTS` in `Game_core.py`

## ⚠️ Troubleshooting

### Common Issues
1. **Missing Images/Sounds**:
   - Ensure all asset files are in correct folders
   - Verify filenames match code references

2. **Pygame Installation Issues**:
   ```bash
   pip uninstall pygame
   pip install pygame --pre
   ```

3. **Window Size Problems**:
   - Game automatically adjusts - try resizing manually
   - For persistent issues, modify `_adjust_window_size()` in `main.py`

4. **Name Validation Errors**:
   - Names must be 3-15 characters
   - Only letters, numbers and spaces allowed
   - Must be unique on leaderboard

### Running Without Audio
If pygame installation fails, the game will still run with full functionality except audio. You'll see "MUSIC OFF" in the top-right corner.

## 👏 Credits
- Game Design and Development: john
- Inspired by: SpongeBob SquarePants by Nickelodeon
- Educational Framework: Common Core Math Standards
- Special Thanks: Python/Tkinter/Pygame communities

**Enjoy your math adventure in Bikini Bottom!**  
*"I'm ready, I'm ready, I'm ready!" - SpongeBob SquarePants*
