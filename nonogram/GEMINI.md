# Project Overview: Illust Logic (Nonogram)

A simple, browser-based Illust Logic (Nonogram) puzzle game implemented as a single-file web application. It features multiple puzzle sizes, a level selection system, and persistent progress tracking.

## Technologies
- **HTML5**: Structure and UI elements.
- **CSS3**: Responsive grid layout using CSS Grid, custom properties for theming, and styling for game states (fill, mark, cleared).
- **Vanilla JavaScript**: Game logic, hint calculation, win detection, and state management.
- **Web Storage API**: Uses `localStorage` to save cleared puzzle IDs.

## Features
- **Level Selection**: Choose between different puzzle sizes (e.g., 5x5, 10x10).
- **Progress Tracking**: Visual indicators (checkmarks) for cleared puzzles, persisted across sessions.
- **How to Play**: Built-in modal guide explaining rules and controls.
- **Responsive Grid**: Cell sizes adjust automatically based on the puzzle dimensions.
- **Dual Controls**: Left-click for toggling states (Fill -> Mark -> Empty) and right-click for quick marking.

## Architecture
The application is self-contained within `index.html`:
- **Data Structure**: Puzzles are stored in a `puzzleData` object, containing binary arrays representing the solution.
- **Hint Logic**: Hints are dynamically generated from the puzzle data for both rows and columns.
- **State Management**: `userState` (a 2D array) tracks the current state of each cell (0: empty, 1: filled, 2: marked).
- **UI Updates**: The `updateView` function synchronizes the DOM with the `userState`.

## Key Files
- `index.html`: The complete application containing HTML structure, CSS styles, and JavaScript logic.

## Usage
### Running the Project
Simply open `index.html` in any modern web browser. No build step or local server is required.

### Development Conventions
- **Naming**: Use descriptive camelCase for JavaScript functions and variables.
- **Styling**: Prefer CSS Grid for layout and CSS variables for consistent colors and sizes.
- **Comments**: Keep logic functions commented, especially for algorithms like hint calculation or win detection.
