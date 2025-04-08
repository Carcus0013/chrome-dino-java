# Chrome Dinosaur Game - Java Implementation
![in-game-screenshot-1](screenshots/screenshot-1.png)

![in-game-screenshot-2](screenshots/screenshot-2.png)

![in-game-screenshot-3](screenshots/screenshot-3.png)

## Description
A Java implementation of Chrome's Offline T-Rex Game with smooth **100 fps** gameplay. This project demonstrates various Object-Oriented Programming concepts through a fun, interactive game.

## Game Features
- Dynamic Background with scrolling land and clouds
- Infinite Gameplay with progressive difficulty
- Multiple Obstacles: Cactuses and Birds (Pterodactyls)
- Player Controls: Jump and Duck
- Game Sounds for jumps and collisions
- Score & High Score tracking with file persistence
- Dynamic jump height based on key holding time
- Quick fall: pressing duck key in midair drops Dino faster
- Pause functionality
- Intro sequence
- Debug mode for development

## Controls
**Jump:** `ARROW UP`, `SPACE`, `W`  
**Duck:** `ARROW DOWN`, `S`  
**Debug:** <code>\`</code> (backtick)  
**Pause:** `ESC`, `P`

## How to Run
1. **Using the JAR file:**
   ```
   java -jar dino.jar
   ```

2. **From source code:**
   ```
   javac src/user_interface/GameWindow.java
   java -cp src user_interface.GameWindow
   ```

## Object-Oriented Programming Concepts Used

### 1. Classes and Objects
The game is built using multiple classes, each responsible for specific functionality:
- `GameWindow`: Main window setup and entry point
- `GameScreen`: Core game logic and rendering
- `Dino`: Player character with behavior and properties
- `Cactuses`/`Birds`: Enemy objects with specific behaviors
- `Land`/`Clouds`: Environment objects
- `Score`: Score tracking system

### 2. Encapsulation
- Private fields with getter/setter methods to control access
- Data hiding for implementation details (e.g., animation frames, collision detection)
- Package organization to group related classes

### 3. Inheritance
- Extends JFrame for the main window (`GameWindow`)
- Extends JPanel for the game screen (`GameScreen`)
- Extends AbstractAction for keyboard input handlers

### 4. Polymorphism
- Method overriding in subclasses
- Common interface for different enemy types
- Runtime behavior determination based on game state

### 5. Abstraction
- High-level methods hide implementation details
- Complex behaviors (like animation, physics) abstracted into dedicated classes
- Clean separation between game logic and rendering

### 6. Interfaces
- ActionListener for handling user input
- Runnable implementation for game loop threading

### 7. Enumerations
- `GameState`: Represents different states (START, INTRO, IN_PROGRESS, OVER, PAUSED)
- `DinoState`: Different states for the dinosaur (RUN, DOWN_RUN, JUMP, DEAD)
- `EnemyType`: Types of enemies (CACTUS, BIRD)

### 8. Composition
- Game objects composed of various components
- Managers (EnemyManager, SoundManager) handling collections of objects
- Complex objects built from simpler ones

### 9. Method Overloading
- Different versions of methods to handle various input types
- Flexible interfaces for game objects

### 10. Exception Handling
- Try-catch blocks for resource loading
- Graceful error handling for file operations

### 11. Multithreading
- Game loop runs on a dedicated thread
- Sound processing in separate threads
- Thread synchronization for consistent gameplay

### 12. Design Patterns
- **Singleton Pattern**: For resource management
- **State Pattern**: For managing game states and dino states
- **Factory Pattern**: For creating enemies
- **Observer Pattern**: For event handling

## Project Structure
- **game_object/**: Contains all game entities
- **manager/**: Classes that manage groups of objects
- **misc/**: Utility classes and enumerations
- **user_interface/**: UI components and rendering
- **util/**: Helper utilities for resources

## Additional Information
High scores are stored in a text file next to the JAR file. Debug mode disables collisions and shows hitboxes and speed information.

## Future Enhancements
- Multiplayer support
- Additional obstacles and power-ups
- Enhanced graphics and animations
- Sound settings
- Difficulty levels
