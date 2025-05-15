# Hangman Game with Physics-Based Rope Simulation

## About the Project

Hangman is a classic word guessing game reimagined with advanced physics simulations. In this implementation, players must guess a hidden word letter by letter before the hangman's rope fully tightens. Unlike traditional hangman games with static imagery, this version features a dynamically simulated rope that responds realistically to tension changes as the game progresses.

Each incorrect guess incrementally increases the tension on the rope, pulling the hangman figure closer to his fate. The visual feedback is immediate and compelling, creating a sense of urgency as players make their guesses. The rope behaves according to real-world physics principles, adding both visual interest and educational value to the classic game concept.

## Physics Simulation: In-Depth Overview

### Spring-Damper System

The rope is modeled as a series of interconnected particles, with each connection behaving as a spring-damper system. This approach creates a physically accurate representation of a rope under tension. The core physics model implements **Hooke's Law** enhanced with damping:

**F = -βv - kx**

Where:
* **F** is the resultant force vector acting on each particle (measured in Newtons)
* **x** is the displacement vector of the spring from its equilibrium position (measured in meters)
* **v** is the velocity vector of the particle (measured in meters per second)
* **k** is the spring constant that determines the rope's stiffness (measured in N/m)
* **β** is the damping coefficient that simulates energy dissipation due to internal friction and air resistance (measured in kg/s)

### Particle System Architecture

Each segment of the rope consists of:
- Mass points (particles) with position, velocity, and acceleration properties
- Spring connections between adjacent particles with configurable rest lengths
- Constraints that maintain the overall structure and prevent unrealistic stretching

### Numerical Integration

The simulation employs Verlet integration to update the position of each particle over time:
1. Forces are calculated based on current positions and velocities
2. Accelerations are derived from forces (a = F/m)
3. Velocities are updated (v = v + a*dt)
4. Positions are updated (p = p + v*dt)
5. Constraints are enforced to maintain rope integrity

### Tension Visualization

As the game progresses and incorrect guesses accumulate:
1. The spring constant (k) increases incrementally
2. Greater tension is visually represented through rope straightening and color changes
3. The rope position updates dynamically, pulling the hangman figure upward
4. Subtle oscillations simulate the natural movement of a tensioned rope

## Gameplay Mechanics

### Word Selection and Difficulty

The game features a comprehensive dictionary organized into difficulty levels:
- **Easy**: 4-5 letter common words from everyday vocabulary
- **Medium**: 6-8 letter words with moderate complexity
- **Hard**: 9+ letter words, including technical terms and obscure vocabulary

The word selection algorithm weighs frequency of usage, ensuring a balanced challenge for players at each level.

### Scoring System

Points are awarded based on multiple factors:
- Length of the word (longer words yield higher base points)
- Difficulty level multiplier (Easy: x1, Medium: x1.5, Hard: x2)
- Time bonus for quick completions
- Penalty reductions for incorrect guesses
- Streak bonuses for consecutive correct games

### Adaptive Difficulty

The game tracks player performance and subtly adjusts:
- Word selection probability based on player's success rate
- Time allowances for different word categories
- Rope tension increment rates per incorrect guess

## User Interface Design

### Visual Components

- **Gallows Structure**: Rendered with weathered wood textures and physical properties
- **Rope Visualization**: Dynamic rendering with tension-responsive thickness and color
- **Character Animation**: The hangman figure responds realistically to rope movements
- **Word Display**: Clear typographic presentation with placeholder and revealed letters
- **Virtual Keyboard**: Color-coded feedback for guessed letters

### Audio Design

- Atmospheric background sounds that intensify with game progress
- Distinct sound effects for correct and incorrect guesses
- Rope tension sounds that correlate with physical simulation
- Success and failure musical sequences

## Technical Implementation Details

### Rendering Engine

The system uses a custom WebGL-based renderer optimized for:
- Efficient particle system updates
- Dynamic rope rendering with adaptive detail levels
- Realistic shadow casting and lighting effects
- Support for both desktop and mobile hardware acceleration

### Physics Calculation Efficiency

To ensure smooth performance across devices:
1. Spatial partitioning techniques reduce unnecessary calculations
2. Adaptive time-stepping adjusts simulation detail based on device capabilities
3. Rope segments far from visible areas use simplified physics models
4. SIMD operations accelerate vector calculations when available

### Memory Management

- Particle pool system prevents garbage collection interruptions
- Texture atlas approach minimizes draw calls
- Efficient data structures optimize force calculations
- Progressive loading of assets based on gameplay needs

## Development Environment

### Technology Stack

- **Frontend**: HTML5, CSS3, WebGL, and JavaScript (ES6+)
- **Build System**: Webpack with hot module replacement
- **Testing Framework**: Jest with custom physics assertion helpers
- **Performance Monitoring**: Custom WebGL profiling tools

### Development Practices

- Test-driven development methodology
- Continuous integration with automated physics regression tests
- Performance benchmarking across device categories
- Accessibility compliance for keyboard navigation and screen readers

## Installation and Setup

```bash
# Clone the repository with depth 1 to minimize download size
git clone --depth 1 https://github.com/unanimousaditya/Hangman-Game.git

# Navigate to the project directory
cd hangman-physics

# Install dependencies with exact versions for consistency
npm ci

# Build optimized production assets
npm run build

# Start the development server with hot reloading
npm start

# Run the test suite
npm test

# Generate performance profile
npm run profile
```

## System Requirements

- **Browser**: Modern browsers with WebGL support (Chrome 80+, Firefox 75+, Safari 13.1+)
- **Processor**: Dual-core 2GHz+ recommended for optimal physics simulation
- **Memory**: 4GB RAM minimum, 8GB recommended
- **Graphics**: Any GPU with WebGL 2.0 support
- **Storage**: 50MB available space for application and cached assets

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Credits

Designed, developed, and maintained by Aditya Raj
