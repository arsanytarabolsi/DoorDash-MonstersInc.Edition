# 🚪 DoorDash — Monsters, Inc. Edition

A **two-player Java board game** built with JavaFX, themed around the world of Monsters, Inc.  
Race your monster across the Scare Floor, collect energy canisters, and reach Cell 99 first to win!

---

## 🎮 Gameplay Overview

- Two players take turns rolling a dice and moving across a 10×10 board (100 cells).
- Each player chooses a **role**: **Scarer** 👹 or **Laugher** 😂 — which affects how Door cells interact with them.
- The first player to **reach Cell 99 with 1000+ energy** wins.

### Special Cells
| Cell Type | Effect |
|---|---|
| 🚪 Door Cell | Gain or lose energy depending on your role |
| 🃏 Card Cell | Draw a random effect card |
| 👾 Monster Cell | Triggers the monster's special ability |
| 🔵 Conveyor Belt | Move forward extra spaces |
| 🧦 Contamination Sock | Move backward and lose energy |

### Cards
- **Confusion Card** — Scrambles movement
- **Energy Steal** — Steal energy from your opponent
- **Shield** — Block the next negative effect
- **Start Over** — Sends a player back to the start
- **Swapper** — Swap positions with your opponent

### Monster Types
| Monster | Ability |
|---|---|
| Dynamo | Accumulates extra energy |
| Dasher | Moves extra spaces |
| MultiTasker | Multiple effects per turn |
| Schemer | Strategic tricky plays |

Each monster has a **Powerup** that costs 500 energy to activate.

---

## 🛠️ Requirements

- **Java 17+**
- **JavaFX 21** — [Download here](https://openjfx.io/)
- An IDE like **Eclipse** or **IntelliJ IDEA** (or run from the command line)

---

## 🚀 How to Run

### Option 1 — Eclipse
1. Open Eclipse → `File` → `Import` → `Existing Projects into Workspace`
2. Select the `DoorDash` folder
3. Right-click the project → `Build Path` → add your JavaFX SDK `lib` folder
4. Run `GUI.java` as a Java Application

### Option 2 — IntelliJ IDEA
1. Open IntelliJ → `File` → `Open` → select the `DoorDash` folder
2. Go to `File` → `Project Structure` → `Libraries` → add your JavaFX `lib` folder
3. Add VM options: `--module-path /path/to/javafx/lib --add-modules javafx.controls,javafx.fxml,javafx.media`
4. Run `GUI.java`

### Option 3 — Command Line
```bash
javac --module-path /path/to/javafx/lib --add-modules javafx.controls,javafx.fxml,javafx.media \
      -d bin src/game/engine/appearance/GUI.java

java --module-path /path/to/javafx/lib --add-modules javafx.controls,javafx.fxml,javafx.media \
     -cp bin game.engine.appearance.GUI
```

> Replace `/path/to/javafx/lib` with the actual path to your JavaFX SDK.

---

## 📁 Project Structure

```
DoorDash/
├── src/
│   └── game/
│       └── engine/
│           ├── appearance/       # GUI, FXML scenes, CSS, assets
│           ├── cards/            # Card types (Confusion, Shield, etc.)
│           ├── cells/            # Cell types (Door, Belt, Sock, etc.)
│           ├── dataloader/       # CSV loading logic
│           ├── exceptions/       # Custom exceptions
│           ├── interfaces/       # CanisterModifier interface
│           └── monsters/         # Monster types (Dasher, Dynamo, etc.)
├── cards.csv                     # Card data
├── cells.csv                     # Board cell data
├── monsters.csv                  # Monster data
└── README.md
```

---

## 👥 Team

**Team 179** — Built as part of a Java OOP course project.

---
This project is for educational purposes.  
Monsters, Inc. characters and theme are property of © Pixar / Disney.
