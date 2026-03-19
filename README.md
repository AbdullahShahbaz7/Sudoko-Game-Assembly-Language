# Assembly-Language

# Sudoku Game in x86 Assembly

A fully functional Sudoku game written in x86 assembly language, featuring a graphical interface, multiple difficulty levels, and interactive gameplay.

## 🎮 Features

### Core Gameplay
- **Three Difficulty Levels**: Easy, Intermediate, and Hard
- **Interactive 9x9 Sudoku Board**: Navigate using arrow keys
- **Note Mode**: Toggle note-taking mode (press 'N') to pencil in possible numbers
- **Undo Function**: Press 'U' to undo your last move
- **Real-time Scoring**: Score points for correct entries

### User Interface
- **Dual-Board Design**: Numbers card displayed at the bottom for reference
- **Visual Feedback**: 
  - Highlighted current cell
  - Red highlighting for incorrect entries
  - Different colors for notes vs. permanent entries
- **Statistics Panel**: Shows current score, mistakes (max 3), timer, and notes status
- **Animated Menus**: Starting screen, level selection, and ending screens with animations

### Audio System
- Victory fanfare when completing a row/column
- Error sound for incorrect inputs
- Level selection confirmation sounds

### Additional Features
- Save/Load screen states
- Timer tracking
- Mistake counter (game ends after 3 mistakes)
- Automatic row/column completion detection
- Game won/loss screens with final statistics

## 🎯 How to Play

### Controls
- **Arrow Keys**: Navigate the board
- **Number Keys (1-9)**: Enter numbers
- **N Key**: Toggle notes mode on/off
- **U Key**: Undo last move
- **Enter**: Select menu options
- **Backspace**: Return to level selection
- **Escape**: Exit to ending screen

### Game Rules
1. Fill the 9x9 grid so that each row, column, and 3x3 box contains all digits 1-9
2. You have a maximum of 3 mistakes
3. Score points for correct entries
4. Complete rows/columns for bonus effects
5. Use notes mode to pencil in possible numbers

## 🏗️ Technical Architecture

### Code Structure
- **Interrupt Handlers**: Custom keyboard and timer ISRs
- **Video Memory Management**: Direct manipulation of 0xB800 video memory
- **Stack-based Undo System**: Tracks up to 100 moves
- **Dual Buffer System**: For smooth screen transitions between board sections
- **Sound Generation**: PC speaker control via PIT

### Key Components
- `starting_screen.asm`: Main menu with animations
- `levels_screen.asm`: Difficulty selection interface
- `print_board.asm`: Board rendering with borders and numbers
- `key_isr.asm`: Keyboard interrupt handlers for both board sections
- `undo.asm`: Undo functionality with stack management
- `sound.asm`: Sound generation for feedback
- `stats.asm`: Score, timer, and mistake tracking

## 🛠️ System Requirements

- **Processor**: x86 architecture
- **Memory**: 64KB+ free memory
- **Display**: 80x25 text mode (VGA compatible)
- **OS**: DOS or compatible environment (DOSBox recommended)

### Running the Game
1. Assemble with NASM: `nasm sudoku.asm -o sudoku.com`
2. Run in DOSBox or compatible environment: `sudoku.com`



## 🎓 Learning Outcomes

This project demonstrates:
- Low-level hardware interaction (keyboard, timer, speaker)
- Video memory manipulation
- Interrupt handling in real mode
- Stack-based data structures
- State management in assembly
- Procedural programming in x86 assembly

## 👥 Contributors

- Abdullah Shahbaz
- Hamza Azam

## 📜 License

This project is open-source and available for educational purposes.

## 🙏 Acknowledgments

- BIOS and DOS interrupt documentation
- x86 assembly programming community
- Classic Sudoku game design
