# Snake Game (x86 Assembly)

## Project Overview

This project is a classic **Snake Game** implemented in **16-bit x86 Assembly Language** for a DOS-based environment. The game runs in text mode and directly interacts with video memory to display graphics.

The objective of the game is to control the snake, eat food to increase the score, and avoid collisions with walls or itself.

---

## Features

* Classic snake gameplay
* Real-time keyboard input using arrow keys
* Dynamic snake movement and growth
* Score tracking system
* Food generation at different locations
* Game over detection
* Text-based UI with messages and instructions

---

## Technologies Used

* **x86 Assembly Language**
* **DOS Interrupts**
* **Text Mode Video Memory (0xB800)**
* Assembler: (e.g., **TASM / MASM / NASM**)
* Emulator: (e.g., **DOSBox**)

---

## How to Run

### 1. Compile the Code

Use an assembler such as NASM:

```bash
nasm -f bin SnakeGame_coalProject.asm -o snake.com
```

### 2. Run the Game

Use DOSBox or any DOS emulator:

```bash
snake.com
```

---

## Controls

* ⬆️ Up Arrow → Move Up
* ⬇️ Down Arrow → Move Down
* ⬅️ Left Arrow → Move Left
* ➡️ Right Arrow → Move Right

---

## Game Rules

* The snake moves continuously in the current direction
* Eat food to grow longer and increase score
* Avoid hitting:

  * Walls
  * The snake’s own body
* The game ends when a collision occurs

---

## Key Concepts Used

### 1. Direct Video Memory Access

The game writes directly to memory address **0xB800** to display characters on screen, instead of using high-level graphics.

### 2. Screen Handling

* Custom `clrscr` function clears the screen
* Text is printed using manually calculated offsets

### 3. String Handling

* Custom implementation of `strlen`
* Printing strings using memory operations (`lodsb`, `stosw`)

### 4. Game Logic

* Snake body stored and updated dynamically
* Movement controlled via keyboard interrupts
* Collision detection implemented manually

---

## Data Structures

* Snake body stored as characters and memory locations
* Variables used for:

  * Snake length
  * Current position
  * Food position
  * Score

---

## Future Improvements

* Add levels and increasing difficulty
* Improve graphics (colors, borders)
* Add sound effects
* Store high scores
* Smooth movement and better collision handling

---

---
