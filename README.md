# 🚀 Smooth Snake Game 🐍 | Pygame

## 🌟 Overview
Welcome to the **Smooth Snake Game**, a classic snake game built using **Python and Pygame**. In this game, you control a snake that moves smoothly around the screen, eating food and growing in length. The game includes **collision detection, score tracking, reverse motion prevention, and a Game Over screen with a delay**.

## 🛠️ Features
- 🎮 **Smooth snake movement**
- 🐍 **Prevent reverse motion** (No moving in the opposite direction instantly)
- 🍎 **Food spawning** at random locations
- 📊 **Score tracking** displayed on the screen
- ⚠️ **Collision detection** (Game over when the snake collides with itself or the boundaries)
- ⏳ **Game Over screen** with a **3-second delay**

## 💪 Technologies Used
- **Python**
- **Pygame** (for rendering, event handling, and game loop control)

## 👨‍💻 How to Install and Run
Follow these steps to run the game on your local system:

### 1️⃣ Prerequisites
Ensure you have Python installed. If not, download and install it from [Python's official website](https://www.python.org/downloads/).

You'll also need Pygame. Install it using:
```sh
pip install pygame
```

### 2️⃣ Clone the Repository
```sh
git clone https://github.com/yourusername/snake-game.git
cd snake-game
```

### 3️⃣ Run the Game
Execute the following command:
```sh
python snake.py
```

## 🚀 Gameplay Controls
- **Arrow Keys** ↑ ↓ ← → - Move the snake in the respective direction
- **Escape (ESC)** - Exit the game

## 😡 Prevent Reverse Motion
To prevent the snake from moving in the opposite direction instantly, we define movement rules:
```python
UP = (0, -velocity)
DOWN = (0, velocity)
LEFT = (-velocity, 0)
RIGHT = (velocity, 0)
```
Before changing direction, we check if the new direction is the opposite of the current one.

## 💀 Game Over Screen
When the snake collides with itself or the walls, the game displays a **Game Over** message and holds the screen for **3 seconds** before exiting:
```python
def game_over():
    screen.fill((255, 255, 255))
    text = font.render("Game Over!", True, (255, 0, 0))
    screen.blit(text, (WIDTH//2 - 50, HEIGHT//2))
    pygame.display.update()
    pygame.time.delay(3000)  # Hold screen for 3 seconds
    pygame.quit()
    quit()
```

## 💪 Contribution
Want to improve the game? Feel free to fork the repository and make enhancements!

## 🌟 Credits
Developed by **[Your Name]**. Inspired by the classic Snake game.

## 🌐 License
This project is licensed under the MIT License.

---
**Enjoy the game and happy coding!** 🚀🐍

