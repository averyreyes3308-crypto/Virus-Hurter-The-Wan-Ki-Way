# 🦠 VIRUS HUNTER - The Wan Ki Way 🦠

A fast-paced, interactive virus hunting game built with vanilla JavaScript, HTML5, and CSS3. Hunt down viruses before they infect you!

## 🎮 Game Overview

**Virus Hunter** is an action-packed clicker game where you must eliminate viruses that spawn from the edges of the screen and travel toward the center. Avoid getting infected by clicking or tapping viruses before they reach your system's core!

### Features
- 🎯 **Click-based gameplay** - Simple but challenging mechanics
- 🎚️ **3 Difficulty Modes** - Easy, Normal, and Hard
- 📈 **Progressive Difficulty** - Viruses increase as you level up
- 💊 **Power-ups** - Heal, Slow viruses, and Double score bonuses
- ✨ **Visual Effects** - Smooth animations, particle effects, and satisfying feedback
- 📱 **Fully Responsive** - Play on desktop, tablet, or mobile
- 🎨 **Neon Aesthetic** - Cyberpunk-inspired visuals with glowing effects

## 🚀 How to Play

### Getting Started
1. Open `index.html` in your web browser
2. Click on a difficulty button (😊 Easy, 😐 Normal, or 😈 Hard)
3. Click "START GAME" to begin

### Game Mechanics
- **Click viruses** (🦠 normal or 😈 dangerous) to eliminate them
- **Earn points** for each virus eliminated
  - Normal viruses: 100 points
  - Dangerous viruses: 150 points
- **Collect power-ups** that randomly spawn after defeating viruses
  - 💊 **Heal** - Restore 30 health points
  - ❄️ **Slow** - Reduce virus speed for 3 seconds
  - ⭐ **Double Score** - Earn bonus 500 points
- **Manage your health** - Don't let viruses reach the center
- **Progress through levels** - Eliminate 5 viruses per level
- **Survive as long as you can** - See how high you can score!

### Game Over
Game ends when your health reaches 0. Your final score, level, and viruses eliminated are displayed.

## 🎯 Difficulty Modes

| Difficulty | Initial Viruses | Speed | Spawn Rate | Damage | Notes |
|-----------|-----------------|-------|-----------|--------|-------|
| **Easy** 😊 | 3 | Slow (1x) | 2 seconds | 5 HP | Great for beginners |
| **Normal** 😐 | 5 | Medium (2x) | 1.5 seconds | 10 HP | Balanced challenge |
| **Hard** 😈 | 8 | Fast (3x) | 1 second | 15 HP | For experienced players |

## 📊 Game Stats

The top panel shows your real-time game statistics:
- **Score** - Total points earned
- **Health** - Current HP (0-100)
- **Level** - Current progression level
- **Viruses Left** - Active viruses on board

## 🎮 Controls

| Action | Control |
|--------|---------|
| **Click Virus** | Mouse click or tap |
| **Collect Power-up** | Mouse click or tap |
| **Pause Game** | Click "Pause" button |
| **Resume Game** | Click "Resume" button |
| **Return to Menu** | Click "Quit" or "Main Menu" button |

## 🛠️ Technical Details

### Technology Stack
- **HTML5** - Semantic markup and canvas elements
- **CSS3** - Modern styling with gradients, animations, and flexbox/grid
- **Vanilla JavaScript** - No dependencies, pure ES6+ code

### Code Structure

#### Classes
1. **VirusHunterGame** - Main game controller
   - Manages game state, UI updates, and game loop
   - Handles difficulty settings and scoring
   - Controls screen transitions

2. **Virus** - Individual virus objects
   - Position and movement logic
   - Collision detection
   - Health and damage system
   - Click interaction handling

3. **PowerUp** - Collectible power-ups
   - Random power-up type selection
   - Collision detection
   - Effect application
   - Auto-expiry timer

### Game Loop
- Runs at ~30 FPS
- Updates virus positions
- Checks collision boundaries
- Processes powerup interactions
- Updates UI elements

## 🎨 Customization

### Adjust Difficulty Settings
Edit the `gameSettings` object in `game.js`:
```javascript
normal: {
    initialViruses: 5,      // Starting virus count
    virusSpeed: 2,          // Movement speed
    spawnRate: 1500,        // Milliseconds between spawns
    healthLoss: 10,         // Damage per escaped virus
    scorePerVirus: 100,     // Base score
    difficultyMultiplier: 1 // Difficulty scaling
}
```

### Change Colors and Themes
Edit CSS color variables in `styles.css`:
- Primary accent: `#00ff88` (neon green)
- Secondary accent: `#00ffff` (cyan)
- Error color: `#ff4444` (red)
- Background: Dark blue gradient

### Customize Virus Types
Modify the virus spawning logic in `Virus` constructor:
```javascript
this.type = Math.random() > 0.7 ? 'dangerous' : 'normal';
// Change 0.7 to adjust dangerous virus spawn rate
```

## 📱 Responsive Design

The game is fully responsive and adapts to:
- Desktop (1920x1080 and higher)
- Tablet (768px - 1024px)
- Mobile (320px - 767px)

All elements scale appropriately and touch controls work seamlessly.

## 🎯 Tips & Strategies

1. **Focus on the center** - Viruses always move toward the center, so watch that area
2. **Prioritize dangerous viruses** - 😈 viruses are worth 50 extra points
3. **Collect power-ups quickly** - They disappear after 5 seconds
4. **Use slow wisely** - The ❄️ freeze effect lasts 3 seconds
5. **Don't ignore health** - Keep an eye on your health bar
6. **Practice Easy mode first** - Build your skills before tackling harder difficulties
7. **Watch for patterns** - Viruses spawn from random edges in predictable paths

## 🐛 Known Issues & Limitations

- Power-ups can't be collected if covered by viruses
- Game runs better on modern browsers with hardware acceleration enabled
- Mobile touch delays may affect timing on slower devices

## 📈 Future Enhancements

Potential features for future updates:
- [ ] Leaderboard system with local storage
- [ ] Different virus types with unique behaviors
- [ ] Boss battles at certain levels
- [ ] Sound effects and background music
- [ ] Upgrades shop (faster clicks, larger hitbox, etc.)
- [ ] Combo multiplier system
- [ ] Daily challenges and achievements
- [ ] Multiplayer / competitive modes

## 📄 License

This project is open source and free to use, modify, and distribute.

## 👾 Credits

**Virus Hunter** - A fun game concept executed with passion and code!

---

## 🎮 Start Playing Now!

Simply open `index.html` in your browser and start hunting viruses. No installation, no dependencies - just pure gaming fun!

**Good luck, and may your defenses be strong!** 🛡️
