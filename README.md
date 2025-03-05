# Rock Paper Scissors 🎮✊📄✂️

![Rock Paper Scissors Banner](https://via.placeholder.com/800x300.png?text=Rock+Paper+Scissors+Game)

## 📝 Overview

Welcome to the **Rock Paper Scissors** game! This is a simple console-based game where you play against the computer in a classic game of Rock, Paper, Scissors. The game consists of **five rounds**, and the player with the highest score wins!

## 🎮 How to Play

1. The game will prompt you to **choose**: `rock`, `paper`, or `scissors`.
2. The **computer randomly selects** one of the three options.
3. The winner is determined based on the classic rules:
   - Rock 🪨 beats Scissors ✂️
   - Scissors ✂️ beats Paper 📄
   - Paper 📄 beats Rock 🪨
4. The game continues for **5 rounds**, and the **final winner is announced**!

## 🔥 Features

✅ Play against a **computer opponent**.
✅ Uses **randomized choices** for the computer.
✅ Keeps **track of scores**.
✅ Case-insensitive input (`rock`, `ROCK`, `rOcK` all work).
✅ Best of **5 rounds** gameplay.

## 🚀 Installation & Setup

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/rock-paper-scissors.git
cd rock-paper-scissors
```

### 2️⃣ Open the HTML file
Simply open `index.html` in a browser to start playing.

### 3️⃣ Open the Console
Since this is a **console-based game**, open the developer console:
- **Windows/Linux:** `F12` or `Ctrl + Shift + I`
- **Mac:** `Cmd + Option + I`
- Navigate to the `Console` tab

## 🧑‍💻 Code Explanation

### `getComputerChoice()`
Generates a random choice (`rock`, `paper`, or `scissors`) for the computer.
```javascript
function getComputerChoice() {
    const choices = ["rock", "paper", "scissors"];
    return choices[Math.floor(Math.random() * 3)];
}
```

### `getHumanChoice()`
Prompts the player to enter their choice and ensures it's lowercase.
```javascript
function getHumanChoice() {
    let choice = prompt("Choose rock, paper, or scissors:").toLowerCase();
    return choice;
}
```

### `playRound(humanChoice, computerChoice)`
Determines the winner of a **single round** and updates the score.
```javascript
function playRound(humanChoice, computerChoice) {
    if (humanChoice === computerChoice) {
        console.log("It's a tie!");
    } else if (
        (humanChoice === "rock" && computerChoice === "scissors") ||
        (humanChoice === "scissors" && computerChoice === "paper") ||
        (humanChoice === "paper" && computerChoice === "rock")
    ) {
        console.log("You win this round!");
        humanScore++;
    } else {