# Tower Building Game 🏢🎮

A classic, physics-based tower building arcade game built for the web. Drop swinging blocks to stack a tower as high as you can! Try to align them perfectly to score double points and build a sturdy, tall tower.

Developed by **[MR Developers](https://mr-developers.github.io/website)**.

---

## 🌟 Features

- **Addictive Gameplay**: Simple one-touch tap or mouse click controls to release the swinging block.
- **Perfect Drops**: Align blocks perfectly with the stack below for bonus points and visual effects.
- **Lives System**: You can make up to 3 failed drops before it is Game Over.
- **Dynamic Physics & Camera**: As your tower grows, the camera dynamically pans up, introducing cloud layers, flying objects, and increasing difficulty.
- **Responsive Layout**: Automatically adjusts resolution and aspect ratios to fit various screen sizes (smartphones, tablets, and desktops).
- **Background Music & Sound Effects**: Immersive audio feedback for drops, perfect drops, swing rotation, and game over.

---

## 🛠️ Tech Stack & Architecture

- **Rendering Engine**: Custom 2D graphics engine powered by `cooljs`.
- **Logic & UI**: Vanilla JavaScript (ES6+) and standard HTML5 Canvas.
- **Styling**: Responsive viewport resizing with custom HSL-themed overlays.
- **Bundler**: Webpack 4 and Babel Preset Env for compiling modern JavaScript features.
- **Local Server**: Express server combined with `opn` for automatic launching and testing in development.
- **DOM Utilities**: Zepto.js (a lightweight alternative to jQuery) for interface manipulation.

---

## 📁 File Structure

```text
├── assets/                # Audio (.mp3) and image (.png, .gif) resources
├── dist/                  # Output directory for Webpack compiled JS bundle
├── src/                   # Source files for game components
│   ├── animateFuncs.js    # Camera scrolling and transition animations
│   ├── background.js      # Stars, sky, and linear gradients background
│   ├── block.js           # Block spawning, drop physics, and alignment logic
│   ├── cloud.js           # Floating cloud background layers
│   ├── constant.js        # Action states, movements, and game constants
│   ├── flight.js          # Flying objects (planes, balloons) at higher altitudes
│   ├── hook.js            # Swing physics, rope, and claw movement
│   ├── index.js           # Main TowerGame configuration and loader
│   ├── line.js            # Ropes, attachment points, and hook constraints
│   ├── tutorial.js        # Instruction screen and arrow overlays
│   └── utils.js           # Canvas calculations and event listeners
├── .babelrc               # Babel compiler configuration
├── index.html             # Entry point / Web interface
├── index.js               # Node.js/Express dev server configuration
├── package.json           # Dependencies and scripts
└── LICENSE                # ISC License file
```

---

## 🚀 Getting Started

Follow these steps to run the game on your local development environment:

### Prerequisites

Make sure you have [Node.js](https://nodejs.org/) (which includes npm) installed.

### Setup Instructions

1. **Clone or Download the Project**:
   Ensure you are in the root directory:
   ```bash
   cd tower_game-master
   ```

2. **Install Dependencies**:
   Install the necessary build tools and libraries:
   ```bash
   npm install
   ```

3. **Build the Assets**:
   Compile the source code using Webpack:
   ```bash
   npm run build
   ```

4. **Start the Local Server**:
   Start the Express server, which will automatically bundle the code and open the game in your default browser at `http://localhost:8082`:
   ```bash
   npm start
   ```

---

## 🎮 How to Play

1. **Start the Game**: Click the "Start" button on the home screen.
2. **Release the Block**: A block swings back and forth from the hook. Tap anywhere on the screen or click your mouse to drop it onto the platform/stack.
3. **Perfect Stacks**: Try to align the center of the swinging block with the block below. A perfect hit triggers a "Perfect!" sound effect and preserves the full width of the tower block.
4. **Three Strikes**: If a block misses the tower completely or slides off, you lose one life (indicated by heart count). The game ends after 3 misses.
5. **High Score**: Share and compete for the highest tower possible!

---

## ⚙️ Customization

You can customize the initial settings of the game inside [index.html](file:///c:/Users/moham/Downloads/tower_game-master/tower_game-master/index.html). The game accepts the following configuration parameters during initialization:

```javascript
const option = {
  width: gameWidth,        // Canvas width
  height: gameHeight,      // Canvas height
  canvasId: 'canvas',      // Target canvas element ID
  soundOn: true,           // Toggle background music and sound effects (true/false)
  setGameScore: function(score) {
    // Callback function when the score updates
  },
  setGameSuccess: function(count) {
    // Callback function when a block is successfully stacked
  },
  setGameFailed: function(missedCount) {
    // Callback function when a block is missed or falls off
  }
}
```

---

## 👥 Credits

Developed and maintained by **[MR Developers](https://mr-developers.github.io/website)**.

---

## 📄 License

This project is licensed under the ISC License. See the [LICENSE](file:///c:/Users/moham/Downloads/tower_game-master/tower_game-master/LICENSE) file for more details.
