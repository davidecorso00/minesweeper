# 💣 Minesweeper — JavaFX Desktop Application

A fully-featured **Minesweeper** game built with Java and JavaFX, following a layered **MVC architecture** with clean separation between backend logic and frontend presentation.

> 📚 Software Engineering — University Project (2024/2025)  
> Author: **Davide Corso**

---

## Features

- **Classic Minesweeper gameplay** — reveal cells, flag bombs, cascade empty cells
- **Save & Load** — persist and resume game state
- **Internationalization (i18n)** — multi-language support (English, Italian)
- **User preferences** — configurable settings stored in properties files
- **Win/Loss detection** — automatic game state management
- **FXML-based UI** — clean separation of layout and logic

## Architecture

The project follows a **3-layer architecture** with strict separation of concerns:

```
┌─────────────────────────────────┐
│           Frontend              │
│  JavaFX Views · Controllers     │
│  FXML Layouts · Event Handlers  │
├─────────────────────────────────┤
│          Application            │
│  Use Cases · App Logic          │
├─────────────────────────────────┤
│           Business              │
│  Game Logic · Grid · Cells      │
│  Save/Load · i18n · Flags       │
├─────────────────────────────────┤
│             Data                │
│  Properties Files · Settings    │
└─────────────────────────────────┘
```

## Tech Stack

- **Java** — core language
- **JavaFX** — desktop UI framework
- **FXML** — declarative UI layouts
- **Maven** — build and dependency management
- **MVC Pattern** — Model-View-Controller design
- **Properties files** — i18n and user preferences

## Project Structure

```
├── backend/
│   └── src/main/java/ch/supsi/minesweeper/
│       ├── application/        # App-level use cases
│       ├── business/           # Core game logic
│       │   ├── Cell.java       # Base cell abstraction
│       │   ├── BombCell.java   # Bomb cell type
│       │   ├── NormalCell.java # Normal cell type
│       │   ├── Grid.java       # Game grid
│       │   ├── GameLogic.java  # Main game engine
│       │   ├── save/           # Save & load logic
│       │   ├── toggleFlag/     # Flag toggling
│       │   ├── selectCell/     # Cell selection
│       │   ├── revealEmptyCell/# Cascade reveal
│       │   ├── won/            # Win condition
│       │   └── lost/           # Loss condition
│       └── data/               # Data access layer
├── frontend/
│   └── src/main/java/ch/supsi/minesweeper/
│       ├── Main.java           # Entry point
│       ├── Model/              # Frontend models
│       ├── controller/         # MVC controllers
│       └── view/               # JavaFX views
├── docs/
│   └── presentation.pdf        # Project presentation
```

## Build & Run

```bash
# Requires Java 17+ and Maven
mvn clean install
mvn javafx:run -pl frontend
```

## License

All rights reserved. This project is shared for portfolio and educational purposes only.
