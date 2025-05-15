
# 🧠 Tetris Game with AI – Python + PyQt5

## 🎮 Overview

This project is a Python implementation of the classic **Tetris** game with a built-in **AI player**. It features a graphical interface built using **PyQt5** and supports both manual play and autonomous AI gameplay.

---

## 📌 Features

- Classic Tetris mechanics with real-time block movement and line clearing
- Heuristic-based AI that can play the game automatically
- Toggle between manual and AI modes
- Visual interface using PyQt5
- Adjustable game speed for testing or human-friendly gameplay
- Next block preview panel

---

## 📂 Project Structure

```
├── tetris_game.py     # Main application & GUI
├── tetris_model.py    # Game rules, shape data, board logic
├── tetris_ai.py       # AI logic and scoring heuristics
```

---

## 🚀 How to Run

### 1. Install Dependencies

Make sure you have Python 3 and the required packages:

```bash
pip install pyqt5 numpy
```

### 2. Run the Game

```bash
python tetris_game.py
```

### 3. Switching Between AI and Manual Play

- To **play manually**:
  - Uncomment this line in `tetris_game.py`:
    ```python
    TETRIS_AI = None
    ```
  - Or comment out this line:
    ```python
    from tetris_ai import TETRIS_AI
    ```

- To **enable AI**:
  Keep this line as is:
  ```python
  from tetris_ai import TETRIS_AI
  ```

---

## 🎮 Controls (Manual Mode)

| Key         | Action               |
|-------------|----------------------|
| `←`         | Move left            |
| `→`         | Move right           |
| `↑`         | Rotate block         |
| `Space`     | Instant drop         |
| `P`         | Pause game           |
| `R`         | Restart after game over |

---

## 🧠 AI Logic

The AI simulates every possible move (rotation + horizontal position) for the current piece, then scores each potential board state using heuristics:

- ✅ Completed lines
- ⚠️ Holes and gaps
- 🔼 Column height and surface bumpiness
- 📊 Height deviation

It selects the move with the best score and executes it autonomously.

---

## 🛠️ Tech Stack

- **Language**: Python 3
- **Libraries**: PyQt5, NumPy
- **Tools**: Visual Studio Code, Git

---

## 👨‍💻 Team Members

- **Muhammad Umer** – AI Development & Heuristics  
- **Sadiq** – Game Logic & Shape Mechanics  
- **Junaid** – UI Development with PyQt5  
- **Subhan** – Testing & AI Integration

---

## 📃 License

This project is for educational purposes. Feel free to use or modify it for learning or portfolio projects.
