# 🎮 Hangman Game

A classic implementation of the Hangman word-guessing game built with HTML, CSS, and JavaScript - challenge your vocabulary while having fun!

## 📖 Description

This Hangman Game is an interactive web-based version of the traditional word-guessing game that brings the pen-and-paper classic to digital life! Players must strategically guess a hidden word letter by letter before the virtual hangman drawing is completed. With each incorrect guess, another piece of the hangman is drawn, bringing you closer to losing the game. The suspense builds with every choice!

The game features an intuitive and visually appealing interface, smooth animations, a variety of word categories to choose from, and sound effects that enhance the gaming experience. Whether you're looking to pass time, improve your vocabulary, or challenge friends, this Hangman Game offers endless entertainment.

## ✨ Features

- 🎯 Interactive gameplay with both on-screen keyboard and physical keyboard support
- 🎭 Visually engaging hangman drawing that progressively appears with each mistake
- 📚 Multiple word categories (Animals, Countries, Sports, Movies, etc.)
- 🏆 Score tracking system to monitor your success rate
- 📱 Fully responsive design that works perfectly on desktop, tablet, and mobile devices
- 🔊 Immersive sound effects for correct guesses, wrong guesses, wins, and losses
- 💡 Optional hint system when you're stuck (with score penalty)
- 🌙 Light/dark mode toggle to reduce eye strain
- ⏱️ Optional timer mode for added challenge

## 🔴 Live Demo

Try the game here: [Hangman Game Live Demo](https://unanimousaditya.github.io/Hangman-Game)

## 🎲 How to Play

1. 🎯 Select a category for your word challenge
2. 🔤 The game randomly selects a word and displays it as underscores
3. ⌨️ Click on the on-screen keyboard letters or use your physical keyboard to guess
4. ✅ Correct guesses reveal the letter in its correct position(s)
5. ❌ Incorrect guesses add another piece to the hangman drawing
6. 🏆 Win by correctly guessing all letters before the hangman is complete
7. 💀 Lose if the hangman drawing is completed (typically after 6 wrong guesses)
8. 🔄 Play again with a new random word!

## 💻 Technologies Used

- ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white) HTML5 for structure
- ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white) CSS3 for styling and animations
- ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black) JavaScript (ES6+) for game logic
- 📱 Responsive design principles for cross-device compatibility
- 🖼️ SVG graphics for the hangman illustrations
- 🔊 Web Audio API for sound effects

## 🚀 Installation and Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/unanimousaditya/Hangman-Game.git
   ```

2. Navigate to the project directory:
   ```bash
   cd Hangman-Game
   ```

3. Open `index.html` in your browser to start playing:
   ```bash
   # On macOS
   open index.html
   
   # On Windows
   start index.html
   
   # On Linux
   xdg-open index.html
   ```

4. No server setup or build process required! The game runs entirely in the browser.

## 📂 Project Structure

```
Hangman-Game/
│
├── index.html           # Main HTML file with game interface
├── css/                 # Stylesheet directory
│   ├── style.css        # Main CSS file for styling
│   ├── animations.css   # CSS animations and transitions
│   └── responsive.css   # Media queries for responsiveness
│
├── js/                  # JavaScript directory
│   ├── script.js        # Core game logic and functionality
│   ├── words.js         # Word categories and collections
│   ├── keyboard.js      # Virtual keyboard handler
│   ├── hangman.js       # Hangman drawing controller
│   └── sounds.js        # Sound effects manager
│
├── assets/              # Media files
│   ├── images/          # Game graphics and SVGs
│   │   ├── hangman/     # Hangman state images
│   │   └── ui/          # UI elements and icons
│   │
│   ├── sounds/          # Game sound effects
│   │   ├── correct.mp3  # Correct guess sound
│   │   ├── wrong.mp3    # Wrong guess sound
│   │   ├── win.mp3      # Win game sound
│   │   └── lose.mp3     # Lose game sound
│   │
│   └── fonts/           # Custom fonts
│
└── README.md            # This documentation file
```

## 🎯 Game Logic

The Hangman Game follows these core principles:

1. 🎲 A word is randomly selected from the chosen category
2. 🧩 The word is initially displayed as a series of underscores
3. 🔠 When a player selects a letter:
   - If the letter is in the word, all instances are revealed
   - If the letter is not in the word, a part of the hangman is drawn
4. 🔄 The game tracks used letters to prevent duplicate guesses
5. 🏁 The game ends when either:
   - All letters are correctly guessed (win)
   - The hangman drawing is completed (lose)

## 🛠️ Contributing

Contributions are enthusiastically welcomed! To contribute:

1. 🍴 Fork the repository
2. 🌱 Create a new branch (`git checkout -b feature/amazing-feature`)
3. ✍️ Make your changes
4. 💾 Commit your changes (`git commit -m 'Add some amazing feature'`)
5. 📤 Push to the branch (`git push origin feature/amazing-feature`)
6. 🔁 Open a Pull Request

### Contribution Guidelines:

- 📏 Follow the existing code style and formatting
- 📝 Add comments to explain complex logic
- ✅ Test your changes thoroughly before submitting
- 🔍 Keep PRs focused on a single feature or bug fix

## 🚀 Future Enhancements

- 🌐 Multiplayer mode to compete with friends
- 🏆 Global leaderboard with player rankings
- 🔤 Custom word submission option
- 🌍 Multiple language support
- 📊 Detailed statistics tracking
- 🎮 Additional game modes (timed challenges, word length challenges)
- 📱 Progressive Web App (PWA) functionality for offline play
- 🔐 User accounts to save progress

## 📜 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 📞 Contact

Aditya - [GitHub](https://github.com/unanimousaditya)

Project Link: [https://github.com/unanimousaditya/Hangman-Game](https://github.com/unanimousaditya/Hangman-Game)

## 👏 Acknowledgments

- 🎮 Inspiration from the classic Hangman game we all played as kids
- 🙌 Thanks to all contributors who have helped improve this project
- 🔤 Word lists compiled from various open sources
- 🎨 UI design inspired by modern gaming interfaces
- 💻 Built with passion for coding and classic games
