# 🎮 Game Development with Raylib and C++: From 2D to 3D 🕹

## 📃Preface

Welcome to "Game Development with Raylib and C++: From 2D to 3D." This book is designed for programmers looking to enter the exciting world of game development using the lightweight and powerful Raylib library with C++. Whether you're new to game development or have experience with other frameworks, this book will guide you through creating both 2D and 3D games with clear explanations and practical examples.

Raylib's philosophy of being simple and easy to use, while still providing robust functionality, makes it an ideal choice for learning game development fundamentals. By the end of this book, you'll have the skills to design and implement your own games and a solid understanding of both 2D and 3D game development principles.

Let's begin the journey!

## Table of Contents

### Part I: Getting Started with Raylib
- Chapter 1: Introduction to Raylib
- Chapter 2: Setting Up Your Development Environment
- Chapter 3: Raylib Fundamentals

### Part II: 2D Game Development
- Chapter 4: 2D Graphics and Rendering
- Chapter 5: Input Handling and User Interaction
- Chapter 6: Project: Simple Pong Game
- Chapter 7: Sprites and Animations
- Chapter 8: Collision Detection in 2D
- Chapter 9: 2D Physics
- Chapter 10: Sound and Music
- Chapter 11: Project: 2D Platformer Game
- Chapter 12: Advanced 2D Techniques

### Part III: Transitioning to 3D
- Chapter 13: Understanding 3D Graphics
- Chapter 14: 3D Rendering in Raylib
- Chapter 15: 3D Models and Texturing
- Chapter 16: Cameras and Perspective

### Part IV: Advanced 3D Game Development
- Chapter 17: 3D Collision Detection
- Chapter 18: 3D Physics
- Chapter 19: Lighting and Shadows
- Chapter 20: Project: First-Person Shooter
- Chapter 21: Advanced Rendering Techniques
- Chapter 22: Project: 3D Racing Game
- Chapter 23: Performance Optimization
- Chapter 24: Artificial Intelligence in Games

### Part V: Beyond the Basics
- Chapter 25: Cross-Platform Development
- Chapter 26: Multiplayer Game Considerations
- Chapter 27: Packaging and Distribution
- Chapter 28: Future Learning Paths

---

# Part I: Getting Started with Raylib

## Chapter 1: Introduction to Raylib

### 1.1 What is Raylib?

Raylib is an open-source, cross-platform library for video game and graphics applications development. Created by Ramon Santamaria, it's designed with a focus on simplicity, making it an excellent choice for beginners and experienced developers alike. Despite its simplicity, Raylib provides a comprehensive set of tools for creating both 2D and 3D games.

#### Key Features of Raylib:

- **Simplicity**: Clean API with minimal dependencies
- **Portability**: Supports Windows, Linux, macOS, Android, and more
- **Performance**: Written in C for speed and efficiency
- **Comprehensive**: Includes modules for graphics, audio, input, and more
- **Self-contained**: Minimal external dependencies
- **Education-oriented**: Easy to learn and use

### 1.2 Why Choose Raylib for Game Development?

Raylib stands out from other game development libraries and frameworks for several reasons:

1. **Low Learning Curve**: Raylib's API is intuitive and straightforward, allowing you to focus on game logic rather than learning complex system interactions.

2. **C and C++ Support**: While Raylib is written in C, it can be easily used with C++, providing flexibility for developers.

3. **Lightweight**: The library has a small footprint, making it ideal for projects where resources are limited.

4. **Open Source**: Being open-source allows for community contributions and ensures the library will remain available.

5. **Cross-Platform**: Write once, deploy anywhere approach saves development time.

### 1.3 Raylib vs. Other Game Frameworks

| Framework | Pros | Cons |
|-----------|------|------|
| **Raylib** | Simple API, lightweight, cross-platform | Less feature-rich than larger engines |
| **SDL** | Widely used, extensive documentation | More complex API, requires more boilerplate |
| **SFML** | Object-oriented, good for C++ | Heavier, more dependencies |
| **Unity** | Complete engine, visual editor | Steeper learning curve, less control over low-level aspects |
| **Unreal** | Industry-standard, powerful | Complex, resource-intensive |

Raylib sits in a sweet spot for educational purposes and smaller indie games, offering enough functionality without overwhelming complexity.

### 1.4 Understanding the Raylib Architecture

Raylib is organized into several modules that handle different aspects of game development:

- **Core**: Window creation, timing, input handling, and other core functionality
- **Shapes**: Basic 2D shape drawing (rectangles, circles, etc.)
- **Textures**: Image loading, texture generation, and manipulation
- **Text**: Font loading and text rendering
- **Models**: 3D model loading and rendering
- **Shaders**: Custom GLSL shader support
- **Audio**: Sound and music loading and playback
- **Physics**: Basic collision detection (with optional external libraries for more complex physics)

### 1.5 Chapter Summary

- Raylib is a lightweight, cross-platform library for game development
- It offers a simple API while still providing powerful features
- The library is particularly suitable for beginners and educational purposes
- Raylib supports both 2D and 3D game development
- Its modular architecture covers all essential aspects of game development

### 1.6 Exercises

1. Research and list three games that have been created using Raylib.
2. Compare Raylib's feature set with another game framework of your choice.
3. Visit the official Raylib repository and explore the examples directory.

## Chapter 2: Setting Up Your Development Environment

### 2.1 System Requirements

Raylib has modest system requirements, making it accessible on a wide range of hardware:

- **Operating System**: Windows, Linux, macOS, FreeBSD, or others
- **Processor**: Any modern CPU (2.0 GHz or better recommended)
- **Memory**: 1GB RAM minimum (2GB or more recommended)
- **Graphics**: OpenGL 3.3 compatible graphics card
- **Storage**: At least 100MB free space for the library and basic projects

### 2.2 Installing Raylib

#### 2.2.1 Windows Installation

There are several ways to install Raylib on Windows:

**Using the installer:**

1. Download the Windows installer from the [Raylib website](https://www.raylib.com).
2. Run the installer and follow the on-screen instructions.
3. The installer will set up Raylib and necessary development tools.

**Using vcpkg:**

```bash
git clone https://github.com/Microsoft/vcpkg.git
cd vcpkg
bootstrap-vcpkg.bat
vcpkg install raylib
```

**Manual installation:**

1. Download the Raylib source code from GitHub.
2. Build the library using CMake or the provided build scripts.
3. Set up your project to link against the built library.

#### 2.2.2 macOS Installation

**Using Homebrew:**

```bash
brew install raylib
```

**Using vcpkg:**

```bash
git clone https://github.com/Microsoft/vcpkg.git
cd vcpkg
./bootstrap-vcpkg.sh
./vcpkg install raylib
```

#### 2.2.3 Linux Installation

**Ubuntu/Debian:**

```bash
sudo apt install libasound2-dev libx11-dev libxrandr-dev libxi-dev libgl1-mesa-dev libglu1-mesa-dev libxcursor-dev libxinerama-dev
git clone https://github.com/raysan5/raylib.git
cd raylib/src
make PLATFORM=PLATFORM_DESKTOP
sudo make install
```

**Arch Linux:**

```bash
sudo pacman -S raylib
```

### 2.3 Setting Up an IDE

#### 2.3.1 Visual Studio

1. Install Visual Studio (Community edition is free).
2. Create a new C++ project.
3. Configure the project to include Raylib's include directories.
4. Link against the Raylib library.
5. Add the Raylib DLL to your project or to your system's PATH.

**Example project configuration:**

```
Include Directories: C:\raylib\include
Library Directories: C:\raylib\lib
Additional Dependencies: raylib.lib
```

#### 2.3.2 Visual Studio Code

1. Install Visual Studio Code.
2. Install the C/C++ extension.
3. Create a new folder for your project.
4. Create a `c_cpp_properties.json` file in a `.vscode` directory:

```json
{
    "configurations": [
        {
            "name": "Win32",
            "includePath": [
                "${workspaceFolder}/**",
                "C:/raylib/include"
            ],
            "defines": [],
            "compilerPath": "C:/MinGW/bin/gcc.exe",
            "cStandard": "c11",
            "cppStandard": "c++17",
            "intelliSenseMode": "gcc-x64"
        }
    ],
    "version": 4
}
```

5. Create a tasks.json file for building:

```json
{
    "version": "2.0.0",
    "tasks": [
        {
            "label": "build",
            "type": "shell",
            "command": "g++",
            "args": [
                "-g", "${file}", "-o", "${fileDirname}/${fileBasenameNoExtension}",
                "-I", "C:/raylib/include",
                "-L", "C:/raylib/lib",
                "-lraylib", "-lopengl32", "-lgdi32", "-lwinmm"
            ],
            "group": {
                "kind": "build",
                "isDefault": true
            },
            "problemMatcher": ["$gcc"]
        }
    ]
}
```

#### 2.3.3 Other IDEs

For other IDEs such as Code::Blocks, CLion, or XCode, the general process is similar:

1. Create a new C++ project.
2. Configure include directories to point to Raylib headers.
3. Set up library linking to the Raylib library.
4. Ensure runtime library access (through PATH or copying DLLs).

### 2.4 Creating Your First Project

Let's create a minimal "Hello, Raylib!" project to verify your setup:

```cpp
#include "raylib.h"

int main() {
    // Initialize window
    const int screenWidth = 800;
    const int screenHeight = 450;
    InitWindow(screenWidth, screenHeight, "Hello, Raylib!");
    
    SetTargetFPS(60);  // Set target frames-per-second
    
    // Main game loop
    while (!WindowShouldClose()) {    // Detect window close button or ESC key
        // Update
        // TODO: Update your variables here
        
        // Draw
        BeginDrawing();
            ClearBackground(RAYWHITE);
            DrawText("Hello, Raylib!", 190, 200, 40, BLACK);
        EndDrawing();
    }
    
    // De-Initialization
    CloseWindow();     // Close window and OpenGL context
    
    return 0;
}
```

This simple program:
1. Creates a window titled "Hello, Raylib!"
2. Sets a target frame rate of 60 FPS
3. Enters a main game loop that continues until the window is closed
4. Clears the screen to white and draws "Hello, Raylib!" text
5. Properly cleans up resources when the program ends

### 2.5 Troubleshooting Common Setup Issues

#### Missing DLLs
- Error: "The program can't start because raylib.dll is missing"
- Solution: Copy raylib.dll to your executable directory or add Raylib's lib directory to your PATH

#### Linker Errors
- Error: "Unresolved external symbol" for Raylib functions
- Solution: Check your linker settings to ensure you're properly linking against the Raylib library

#### Compilation Errors
- Error: "Cannot open include file: 'raylib.h'"
- Solution: Verify your include path settings

#### OpenGL Issues
- Error: "Failed to initialize OpenGL device"
- Solution: Update your graphics drivers or check that your system supports OpenGL 3.3

### 2.6 Chapter Summary

- Raylib can be installed on various platforms using different methods
- Setting up your development environment involves installing Raylib and configuring your IDE
- A basic Raylib program creates a window, handles a game loop, and renders content
- Common setup issues are usually related to incorrect paths or missing dependencies

### 2.7 Exercises

1. Set up Raylib on your preferred platform and verify the installation by running a basic example.
2. Modify the "Hello, Raylib!" example to display your name and change the background color.
3. Explore the examples provided with Raylib and try to compile and run at least three of them.

## Chapter 3: Raylib Fundamentals

### 3.1 Understanding the Game Loop

The game loop is the heart of any game. It's a continuous cycle that runs as long as the game is active, typically handling three main tasks:

1. **Processing Input**: Detecting and responding to user input like keyboard presses or mouse movements
2. **Updating Game State**: Modifying game objects, checking collisions, updating AI, etc.
3. **Rendering**: Drawing the current state of the game to the screen

In Raylib, a basic game loop looks like this:

```cpp
while (!WindowShouldClose()) {
    // Process Input
    // ...
    
    // Update Game State
    // ...
    
    // Render
    BeginDrawing();
        ClearBackground(RAYWHITE);
        // Draw game elements here
    EndDrawing();
}
```

The `WindowShouldClose()` function returns true when the user attempts to close the window or presses the ESC key, providing a convenient way to exit the loop.

### 3.2 Core Functions and Data Types

#### 3.2.1 Initialization and Shutdown

```cpp
// Initialize window
InitWindow(width, height, title);

// Set target FPS
SetTargetFPS(fps);

// Close window and unload resources
CloseWindow();
```

#### 3.2.2 Basic Data Types

Raylib provides several data types to represent game elements:

- **Vector2**: A 2D vector with x and y components
- **Vector3**: A 3D vector with x, y, and z components
- **Vector4**: A 4D vector often used for quaternions
- **Rectangle**: A rectangle defined by x, y, width, and height
- **Color**: An RGBA color
- **Image**: Raw image data
- **Texture2D**: GPU texture data
- **Camera2D**: 2D camera for transform operations
- **Camera3D**: 3D camera for perspective viewing

Example usage:

```cpp
// Create a Vector2
Vector2 position = { 100.0f, 200.0f };

// Create a Rectangle
Rectangle rect = { 50.0f, 50.0f, 200.0f, 100.0f };

// Define a Color
Color purple = { 200, 122, 255, 255 };  // R, G, B, A values
// Or use predefined colors
Color red = RED;
```

### 3.3 Drawing Basic Shapes

Raylib makes it easy to draw basic shapes:

```cpp
// Draw a circle
DrawCircle(centerX, centerY, radius, color);

// Draw a rectangle
DrawRectangle(posX, posY, width, height, color);

// Draw a line
DrawLine(startPosX, startPosY, endPosX, endPosY, color);

// Draw a triangle
DrawTriangle(v1, v2, v3, color);

// Draw a polygon
DrawPoly(center, sides, radius, rotation, color);
```

Example:

```cpp
void DrawSimpleScene() {
    ClearBackground(RAYWHITE);
    
    // Draw shapes
    DrawRectangle(100, 100, 200, 80, RED);
    DrawCircle(300, 200, 60, BLUE);
    DrawTriangle(
        (Vector2){ 500, 100 },
        (Vector2){ 450, 200 },
        (Vector2){ 550, 200 },
        GREEN
    );
    
    // Draw a line
    DrawLine(50, 300, 600, 300, BLACK);
}
```

### 3.4 Handling Input

Raylib provides functions for detecting keyboard, mouse, and gamepad input:

#### 3.4.1 Keyboard Input

```cpp
// Check if a key is being pressed
if (IsKeyDown(KEY_RIGHT)) {
    playerPosition.x += 2.0f;
}

// Check if a key has been pressed once
if (IsKeyPressed(KEY_SPACE)) {
    FireWeapon();
}

// Check if a key has been released
if (IsKeyReleased(KEY_Z)) {
    ToggleZoom();
}
```

#### 3.4.2 Mouse Input

```cpp
// Get mouse position
Vector2 mousePosition = GetMousePosition();

// Check if mouse button is down
if (IsMouseButtonDown(MOUSE_LEFT_BUTTON)) {
    DragObject(mousePosition);
}

// Check if mouse button was pressed once
if (IsMouseButtonPressed(MOUSE_RIGHT_BUTTON)) {
    OpenContextMenu(mousePosition);
}

// Get mouse wheel movement
float wheelMove = GetMouseWheelMove();
if (wheelMove != 0) {
    ZoomCamera(wheelMove);
}
```

#### 3.4.3 Touch Input (for mobile platforms)

```cpp
// Check if touch input is available
if (IsTouchDevice()) {
    // Get number of touch points
    int touchPointCount = GetTouchPointCount();
    
    // Get position of first touch point
    Vector2 touchPosition = GetTouchPosition(0);
}
```

### 3.5 Working with Time

Managing time is crucial for creating smooth animations and gameplay:

```cpp
// Get time since last frame (delta time)
float deltaTime = GetFrameTime();

// Update position based on delta time
position.x += speed * deltaTime;

// Get elapsed time since InitWindow()
double totalTime = GetTime();
```

Using delta time ensures that your game runs at the same speed regardless of frame rate.

### 3.6 Understanding Coordinates and Transformations

#### 3.6.1 2D Coordinate System

In Raylib's 2D coordinate system:
- The origin (0, 0) is at the top-left corner of the window
- X increases to the right
- Y increases downward

#### 3.6.2 Basic Transformations

```cpp
// Draw with rotation
DrawTexturePro(
    texture,
    sourceRec,
    destRec,
    origin,    // Point around which to rotate
    rotation,  // Rotation angle in degrees
    tint
);

// Using matrices for transformations
Matrix transform = MatrixIdentity();
transform = MatrixMultiply(transform, MatrixRotateZ(rotation));
transform = MatrixMultiply(transform, MatrixTranslate(position.x, position.y, 0));
```

### 3.7 Your First Complete Game: Ball Bounce

Let's create a simple game where a ball bounces around the screen:

```cpp
#include "raylib.h"

int main(void) {
    // Initialization
    const int screenWidth = 800;
    const int screenHeight = 450;

    InitWindow(screenWidth, screenHeight, "Ball Bounce");

    // Ball properties
    Vector2 ballPosition = { (float)screenWidth/2, (float)screenHeight/2 };
    Vector2 ballSpeed = { 5.0f, 4.0f };
    int ballRadius = 20;
    Color ballColor = RED;

    SetTargetFPS(60);               // Set target frames-per-second

    // Main game loop
    while (!WindowShouldClose()) {  // Detect window close button or ESC key
        // Update
        ballPosition.x += ballSpeed.x;
        ballPosition.y += ballSpeed.y;

        // Check bounds collision
        if ((ballPosition.x >= (screenWidth - ballRadius)) || 
            (ballPosition.x <= ballRadius)) {
            ballSpeed.x *= -1.0f;
        }
        if ((ballPosition.y >= (screenHeight - ballRadius)) || 
            (ballPosition.y <= ballRadius)) {
            ballSpeed.y *= -1.0f;
        }

        // Draw
        BeginDrawing();
            ClearBackground(RAYWHITE);
            
            DrawCircleV(ballPosition, ballRadius, ballColor);
            DrawText("Ball Bounce Example", 10, 10, 20, DARKGRAY);
            
        EndDrawing();
    }

    // De-Initialization
    CloseWindow();        // Close window and OpenGL context

    return 0;
}
```

This example demonstrates:
- Creating a window
- Implementing a simple physics simulation
- Handling collision detection
- Drawing shapes
- Maintaining a game loop

### 3.8 Chapter Summary

- The game loop is the foundation of any game, handling input, updates, and rendering
- Raylib provides essential data types like Vector2, Rectangle, and Color
- Basic shape drawing functions allow quick visualization
- Input handling can detect keyboard, mouse, and touch interactions
- Time management is crucial for consistent gameplay across different devices
- Understanding the coordinate system helps with positioning and transformations

### 3.9 Exercises

1. Modify the Ball Bounce example to add user control over the ball using arrow keys.
2. Create a simple drawing program that allows users to draw shapes with the mouse.
3. Implement a digital clock that displays the current system time.
4. Create a program that simulates multiple bouncing balls with different colors and sizes.

### 3.10 Challenge Project: Pong Prototype

Create a basic Pong game prototype with the following features:
- Two paddles controlled by keyboard (W/S for left player, Up/Down arrows for right player)
- A ball that bounces off walls and paddles
- Basic scoring system
- Simple menu screen

---

# Part II: 2D Game Development

## Chapter 4: 2D Graphics and Rendering

### 4.1 Loading and Drawing Images

In game development, you'll often work with images rather than simple shapes. Raylib makes image handling straightforward with its texture system.

#### 4.1.1 Loading Textures

```cpp
// Load texture from file
Texture2D texture = LoadTexture("resources/my_texture.png");

// Later, unload the texture when no longer needed
UnloadTexture(texture);
```

#### 4.1.2 Drawing Textures

```cpp
// Basic texture drawing
DrawTexture(texture, posX, posY, WHITE);

// Draw part of a texture (useful for sprite sheets)
Rectangle sourceRec = { 0, 0, 64, 64 };  // Part of the texture to use
Rectangle destRec = { 100, 100, 128, 128 };  // Where to draw it (with scaling)
Vector2 origin = { 0, 0 };  // Origin for rotation/scaling
float rotation = 0.0f;
DrawTexturePro(texture, sourceRec, destRec, origin, rotation, WHITE);
```

#### 4.1.3 Working with Images

Raylib distinguishes between `Image` (CPU memory) and `Texture2D` (GPU memory):

```cpp
// Load image from file
Image image = LoadImage("resources/my_image.png");

// Manipulate the image (CPU-side)
ImageResize(&image, 200, 200);
ImageDraw(&image, sourceImage, sourceRec, destRec, tint);
ImageFlipVertical(&image);

// Convert to texture (GPU-side) for rendering
Texture2D texture = LoadTextureFromImage(image);

// Unload the image data when no longer needed
UnloadImage(image);
```

### 4.2 Working with Colors and Transparency

#### 4.2.1 Color Basics

```cpp
// Define colors using RGBA components (0-255)
Color myRed = { 230, 41, 55, 255 };

// Using predefined colors
Color skyBlue = SKYBLUE;

// Changing alpha for transparency
Color semiTransparent = { 255, 255, 255, 128 };  // 50% transparent white
```

#### 4.2.2 Color Manipulation

```cpp
// Fade a color
Color fadedColor = Fade(RED, 0.5f);  // 50% transparent red

// Color operations
Color colorA = { 100, 100, 100, 255 };
Color colorB = { 50, 50, 50, 255 };
Color added = ColorAdd(colorA, colorB);
Color multiplied = ColorMultiply(colorA, colorB);
```

#### 4.2.3 Using Transparency

```cpp
// Draw semi-transparent shapes
DrawRectangle(100, 100, 200, 100, Fade(RED, 0.5f));

// Set blend mode for advanced transparency effects
BeginBlendMode(BLEND_ADDITIVE);
    DrawTexture(glowTexture, posX, posY, WHITE);
EndBlendMode();
```

### 4.3 Text Rendering

#### 4.3.1 Basic Text Drawing

```cpp
// Simple text drawing
DrawText("Hello, Raylib!", 100, 100, 20, BLACK);

// Formatted text
DrawTextEx(font, TextFormat("Score: %d", score), position, fontSize, spacing, color);
```

#### 4.3.2 Working with Fonts

```cpp
// Load a custom font
Font customFont = LoadFont("resources/myfont.ttf");

// Draw using custom font
DrawTextEx(customFont, "Custom Font Text", position, fontSize, spacing, color);

// Unload when done
UnloadFont(customFont);
```

#### 4.3.3 Text Measurements

```cpp
// Measure text to position it properly
Vector2 textSize = MeasureTextEx(font, "Center Me", fontSize, spacing);
Vector2 textPosition = {
    screenWidth/2 - textSize.x/2,  // Center horizontally
    screenHeight/2 - textSize.y/2  // Center vertically
};
```

### 4.4 Using Cameras in 2D

The Camera2D system allows you to implement scrolling, zooming, and other transformation effects.

#### 4.4.1 Setting Up a 2D Camera

```cpp
// Initialize camera
Camera2D camera = { 0 };
camera.target = (Vector2){ player.x, player.y };  // Camera follows this point
camera.offset = (Vector2){ screenWidth/2, screenHeight/2 };  // Camera center point
camera.rotation = 0.0f;
camera.zoom = 1.0f;
```

#### 4.4.2 Using the Camera

```cpp
// Begin camera mode
BeginMode2D(camera);
    // Draw world elements (these will be affected by camera)
    DrawTexture(backgroundTexture, 0, 0, WHITE);
    DrawRectangleRec(playerRec, RED);
    DrawMap(gameMap);
EndMode2D();

// Draw UI elements (these will NOT be affected by camera)
DrawText("Score: 100", 10, 10, 20, BLACK);
```

#### 4.4.3 Camera Movement and Zoom

```cpp
// Update camera to follow player
camera.target = player.position;

// Smooth camera following
camera.target.x = camera.target.x + 0.2f * (player.position.x - camera.target.x);
camera.target.y = camera.target.y + 0.2f * (player.position.y - camera.target.y);

// Camera zoom with mouse wheel
float wheel = GetMouseWheelMove();
if (wheel != 0) {
    camera.zoom += wheel * 0.05f;
    if (camera.zoom < 0.1f) camera.zoom = 0.1f;
    if (camera.zoom > 3.0f) camera.zoom = 3.0f;
}

// Camera rotation
if (IsKeyDown(KEY_R)) camera.rotation += 1.0f;
```

### 4.5 Framebuffers and Render Textures

Render textures allow you to draw to an off-screen texture, which can be used for effects, minimaps, and more.

```cpp
// Create a render texture
RenderTexture2D target = LoadRenderTexture(400, 300);

// Draw to render texture
BeginTextureMode(target);
    ClearBackground(RAYWHITE);
    DrawText("This is drawn to a texture", 10, 10, 20, BLACK);
    DrawCircle(200, 150, 50, RED);
EndTextureMode();

// Draw the render texture to the screen
DrawTextureRec(
    target.texture,
    (Rectangle){ 0, 0, target.texture.width, -target.texture.height },
    (Vector2){ 0, 0 },
    WHITE
);

// Unload when done
UnloadRenderTexture(target);
```

### 4.6 Implementing a Tile-Based Game World

Tile-based worlds are common in many 2D games. Here's how to implement a simple tile system:

```cpp
#define TILE_SIZE 32
#define MAP_WIDTH 50
#define MAP_HEIGHT 50

typedef enum {
    TILE_EMPTY = 0,
    TILE_WALL,
    TILE_WATER,
    TILE_GRASS
} TileType;

// Map data
int map[MAP_HEIGHT][MAP_WIDTH] = { 0 };

// Tile textures
Texture2D tileTextures[4];

void LoadTileTextures() {
    tileTextures[TILE_EMPTY] = LoadTexture("resources/empty.png");
    tileTextures[TILE_WALL] = LoadTexture("resources/wall.png");
    tileTextures[TILE_WATER] = LoadTexture("resources/water.png");
    tileTextures[TILE_GRASS] = LoadTexture("resources/grass.png");
}

void DrawMap(Camera2D camera) {
    // Calculate which tiles are visible in the current view
    int startX = (int)fmax(0, camera.target.x - camera.offset.x / camera.zoom);
    int startY = (int)fmax(0, camera.target.y - camera.offset.y / camera.zoom);
    int endX = (int)fmin(MAP_WIDTH, startX + screenWidth / (TILE_SIZE * camera.zoom) + 2);
    int endY = (int)fmin(MAP_HEIGHT, startY + screenHeight / (TILE_SIZE * camera.zoom) + 2);
    
    // Only draw visible tiles
    for (int y = startY; y < endY; y++) {
        for (int x = startX; x < endX; x++) {
            int tileType = map[y][x];
            DrawTexture(tileTextures[tileType], x * TILE_SIZE, y * TILE_SIZE, WHITE);
        }
    }
}
```

### 4.7 Advanced Drawing Techniques

#### 4.7.1 Drawing Primitives

```cpp
// Draw line with thickness
DrawLineEx(start, end, 5.0f, RED);

// Draw a curve
DrawLineBezier(start, end, 2.0f, BLUE);

// Draw circle with gradient
DrawCircleGradient(centerX, centerY, radius, RED, BLUE);

// Draw polygon
DrawPoly(center, 6, radius, rotation, PURPLE);  // Hexagon
```

#### 4.7.2 Shaders

Raylib supports GLSL shaders for advanced visual effects:

```cpp
// Load shader
Shader shader = LoadShader(NULL, "resources/shaders/bloom.fs");

// Get shader uniform locations
int resolutionLoc = GetShaderLocation(shader, "resolution");

// Set shader uniforms
float resolution[2] = { (float)screenWidth, (float)screenHeight };
SetShaderValue(shader, resolutionLoc, resolution, SHADER_UNIFORM_VEC2);

// Use shader for drawing
BeginShaderMode(shader);
    DrawTexture(texture, 0, 0, WHITE);
EndShaderMode();

// Unload shader
UnloadShader(shader);
```


### 4.8 Chapter Summary (continued)
- Color and transparency effects add visual appeal to your games
- Text rendering allows displaying scores, messages, and other information
- Camera2D enables scrolling, zooming, and other view transformations
- Render textures allow off-screen rendering for advanced effects
- Tile-based worlds are an efficient way to create large game environments
- Advanced drawing techniques like primitives and shaders enable unique visual styles

### 4.9 Exercises

1. Create a program that loads and displays a sprite sheet, showing different frames in sequence.
2. Implement a simple camera system that follows a player character around a larger map.
3. Create a tile-based map editor that allows placing different tiles with the mouse.
4. Experiment with blending modes to create visual effects like explosions or magic spells.
5. Use render textures to create a minimap for a larger game world.

### 4.10 Challenge Project: Retro Arcade Background

Create a dynamic retro arcade background with the following features:
- Scrolling grid lines
- Floating geometric shapes with varying sizes and rotations
- Pulsating colors using sine waves
- Text that moves across the screen
- Particle effects that respond to mouse movement

## Chapter 5: Input Handling and User Interaction

### 5.1 Understanding Input in Games

Good input handling is crucial for creating responsive games. Players interact with games through various devices:

- Keyboards
- Mice
- Gamepads/controllers
- Touch screens (for mobile platforms)
- Motion sensors (less common)

Input handling typically involves these steps:
1. Detecting when input occurs
2. Mapping that input to game actions
3. Responding appropriately in the game world

Raylib provides a comprehensive set of functions for handling different input types.

### 5.2 Keyboard Input in Depth

#### 5.2.1 Key States

Raylib distinguishes between different key states:

```cpp
// Check if a key is currently pressed down
if (IsKeyDown(KEY_RIGHT)) {
    // Continuous action (like movement)
    player.x += 5.0f;
}

// Check if a key was just pressed (one-time trigger)
if (IsKeyPressed(KEY_SPACE)) {
    // One-time action (like jumping or firing)
    player.Jump();
}

// Check if a key was just released
if (IsKeyReleased(KEY_Z)) {
    // Action on release (like dropping an item)
    player.DropItem();
}

// Check if a key is not being pressed
if (!IsKeyDown(KEY_LEFT) && !IsKeyDown(KEY_RIGHT)) {
    // No movement keys pressed, maybe set player to idle animation
    player.SetState(IDLE);
}
```

#### 5.2.2 Getting Key Press Information

```cpp
// Get the last key pressed
int key = GetKeyPressed();
if (key != 0) {
    printf("Key pressed: %d\n", key);
}

// Check for any key press
if (IsAnyKeyPressed()) {
    // React to any key press
}
```

#### 5.2.3 Text Input

For games that need to capture text input (like entering a player name):

```cpp
// Set a key to exit text input mode
if (IsKeyPressed(KEY_ENTER)) {
    textInputMode = !textInputMode;
}

// When in text input mode
if (textInputMode) {
    int key = GetCharPressed();
    
    // Add characters to input string
    while (key > 0) {
        if ((key >= 32) && (key <= 125) && (textLength < MAX_INPUT_CHARS)) {
            name[textLength] = (char)key;
            name[textLength+1] = '\0';
            textLength++;
        }
        
        key = GetCharPressed();  // Check for more characters
    }
    
    // Handle backspace
    if (IsKeyPressed(KEY_BACKSPACE)) {
        if (textLength > 0) {
            textLength--;
            name[textLength] = '\0';
        }
    }
}
```

### 5.3 Mouse Input in Depth

#### 5.3.1 Mouse Position and Movement

```cpp
// Get current mouse position
Vector2 mousePos = GetMousePosition();

// Get mouse delta (movement since last frame)
Vector2 mouseDelta = GetMouseDelta();

// Get mouse X/Y separately
int mouseX = GetMouseX();
int mouseY = GetMouseY();
```

#### 5.3.2 Mouse Buttons

Similar to keyboard keys, mouse buttons have different states:

```cpp
// Check if mouse button is currently down
if (IsMouseButtonDown(MOUSE_LEFT_BUTTON)) {
    // Continuous action (like dragging)
    DragObject(mousePos);
}

// Check if mouse button was just pressed
if (IsMouseButtonPressed(MOUSE_RIGHT_BUTTON)) {
    // One-time action (like selecting)
    SelectObject(mousePos);
}

// Check if mouse button was just released
if (IsMouseButtonReleased(MOUSE_LEFT_BUTTON)) {
    // Action on release (like placing an object)
    PlaceObject(mousePos);
}
```

#### 5.3.3 Mouse Wheel

```cpp
// Get mouse wheel movement (vertical)
float wheelMove = GetMouseWheelMove();

// Use wheel for zooming
if (wheelMove != 0) {
    camera.zoom += wheelMove * 0.05f;
    // Clamp zoom to reasonable values
    if (camera.zoom < 0.1f) camera.zoom = 0.1f;
    if (camera.zoom > 3.0f) camera.zoom = 3.0f;
}
```

#### 5.3.4 Cursor Visibility and Constraints

```cpp
// Hide the system cursor (for custom cursors)
HideCursor();

// Use a custom cursor texture
DrawTexture(cursorTexture, mouseX, mouseY, WHITE);

// Show the system cursor again
ShowCursor();

// Constrain cursor to a region (useful for game windows)
Rectangle bounds = { 100, 100, 600, 400 };
EnableCursor();  // Make sure cursor is enabled
ClampCursor(&bounds);

// Disable cursor clamping
DisableCursorConstraint();
```

### 5.4 Gamepad Input

Raylib provides comprehensive gamepad support for various controllers.

#### 5.4.1 Detecting Gamepads

```cpp
// Check if a gamepad is available
if (IsGamepadAvailable(0)) {  // 0 is the first gamepad
    // Gamepad is connected
    const char *gamepadName = GetGamepadName(0);
    DrawText(TextFormat("Gamepad detected: %s", gamepadName), 10, 10, 20, BLACK);
}
```

#### 5.4.2 Gamepad Buttons

```cpp
// Check if a gamepad button is pressed
if (IsGamepadButtonPressed(0, GAMEPAD_BUTTON_RIGHT_FACE_DOWN)) {  // 'A' on Xbox
    player.Jump();
}

// Check if a gamepad button is down
if (IsGamepadButtonDown(0, GAMEPAD_BUTTON_LEFT_TRIGGER_1)) {  // Left bumper
    player.Shield();
}

// Check if a gamepad button is released
if (IsGamepadButtonReleased(0, GAMEPAD_BUTTON_RIGHT_TRIGGER_1)) {  // Right bumper
    player.SwapWeapon();
}
```

#### 5.4.3 Gamepad Axes (Analog Sticks)

```cpp
// Get axis values (-1.0 to 1.0)
float leftStickX = GetGamepadAxisMovement(0, GAMEPAD_AXIS_LEFT_X);
float leftStickY = GetGamepadAxisMovement(0, GAMEPAD_AXIS_LEFT_Y);

// Apply deadzone to ignore small movements
float deadzone = 0.2f;
if (fabs(leftStickX) < deadzone) leftStickX = 0;
if (fabs(leftStickY) < deadzone) leftStickY = 0;

// Use for player movement
player.velocity.x = leftStickX * player.speed;
player.velocity.y = leftStickY * player.speed;

// Camera control with right stick
float rightStickX = GetGamepadAxisMovement(0, GAMEPAD_AXIS_RIGHT_X);
float rightStickY = GetGamepadAxisMovement(0, GAMEPAD_AXIS_RIGHT_Y);

if (fabs(rightStickX) > deadzone || fabs(rightStickY) > deadzone) {
    camera.rotation += rightStickX * 2.0f;
}
```

### 5.5 Touch Input for Mobile Platforms

Raylib supports touch input for mobile platforms like Android and iOS.

```cpp
// Check if current device has touch capabilities
if (IsTouchDevice()) {
    // Get number of current touches
    int touchCount = GetTouchPointCount();
    
    // Process all current touches
    for (int i = 0; i < touchCount; i++) {
        Vector2 touchPos = GetTouchPosition(i);
        
        // Check if touch is within button area
        if (CheckCollisionPointRec(touchPos, buttonBounds)) {
            // Button touched
            buttonPressed = true;
        }
    }
}
```

#### 5.5.1 Implementing Multi-Touch Gestures

```cpp
// Enable gesture detection (call once at initialization)
SetGesturesEnabled(GESTURE_PINCH_IN | GESTURE_PINCH_OUT | GESTURE_SWIPE_RIGHT);

// Check for specific gestures
if (IsGestureDetected(GESTURE_PINCH_IN)) {
    // Zoom out
    camera.zoom -= 0.1f;
    if (camera.zoom < 0.1f) camera.zoom = 0.1f;
}

if (IsGestureDetected(GESTURE_PINCH_OUT)) {
    // Zoom in
    camera.zoom += 0.1f;
    if (camera.zoom > 3.0f) camera.zoom = 3.0f;
}

// Get gesture hold duration
float holdTime = GetGestureHoldDuration();
if (holdTime > 1.0f) {  // Held for more than 1 second
    // Activate special action
    player.SpecialAttack();
}

// Get drag vector
Vector2 dragVector = GetGestureDragVector();
camera.target.x -= dragVector.x;
camera.target.y -= dragVector.y;
```

### 5.6 Creating a Menu System

A good menu system enhances user experience. Let's implement a simple game menu:

```cpp
typedef enum {
    MENU_STATE_MAIN,
    MENU_STATE_SETTINGS,
    MENU_STATE_CREDITS,
    MENU_STATE_PLAYING,
    MENU_STATE_PAUSED
} MenuState;

typedef struct {
    Rectangle bounds;
    const char *text;
    bool selected;
} Button;

// Current menu state
MenuState currentMenu = MENU_STATE_MAIN;

// Main menu buttons
Button mainMenuButtons[3] = {
    { { 300, 150, 200, 50 }, "Play", false },
    { { 300, 220, 200, 50 }, "Settings", false },
    { { 300, 290, 200, 50 }, "Exit", false }
};

void UpdateMainMenu() {
    Vector2 mousePoint = GetMousePosition();
    
    // Update button states based on mouse position
    for (int i = 0; i < 3; i++) {
        mainMenuButtons[i].selected = CheckCollisionPointRec(mousePoint, mainMenuButtons[i].bounds);
        
        // Button logic
        if (mainMenuButtons[i].selected && IsMouseButtonReleased(MOUSE_LEFT_BUTTON)) {
            switch (i) {
                case 0: currentMenu = MENU_STATE_PLAYING; break;
                case 1: currentMenu = MENU_STATE_SETTINGS; break;
                case 2: CloseWindow(); break;
            }
        }
    }
}

void DrawMainMenu() {
    ClearBackground(RAYWHITE);
    
    DrawText("MY AWESOME GAME", 250, 80, 30, BLACK);
    
    // Draw buttons
    for (int i = 0; i < 3; i++) {
        DrawRectangleRec(
            mainMenuButtons[i].bounds, 
            mainMenuButtons[i].selected ? SKYBLUE : LIGHTGRAY
        );
        
        // Calculate text position to center it in the button
        Vector2 textSize = MeasureTextEx(GetFontDefault(), mainMenuButtons[i].text, 20, 1);
        Vector2 textPos = {
            mainMenuButtons[i].bounds.x + mainMenuButtons[i].bounds.width/2 - textSize.x/2,
            mainMenuButtons[i].bounds.y + mainMenuButtons[i].bounds.height/2 - textSize.y/2
        };
        
        DrawTextEx(GetFontDefault(), mainMenuButtons[i].text, textPos, 20, 1, BLACK);
    }
}

// Main game loop with menu state machine
void GameLoop() {
    while (!WindowShouldClose()) {
        // Update based on current menu state
        switch (currentMenu) {
            case MENU_STATE_MAIN:
                UpdateMainMenu();
                break;
            case MENU_STATE_SETTINGS:
                UpdateSettingsMenu();
                break;
            case MENU_STATE_PLAYING:
                UpdateGame();
                if (IsKeyPressed(KEY_ESCAPE)) currentMenu = MENU_STATE_PAUSED;
                break;
            case MENU_STATE_PAUSED:
                UpdatePauseMenu();
                break;
            default: break;
        }
        
        // Draw based on current menu state
        BeginDrawing();
            switch (currentMenu) {
                case MENU_STATE_MAIN:
                    DrawMainMenu();
                    break;
                case MENU_STATE_SETTINGS:
                    DrawSettingsMenu();
                    break;
                case MENU_STATE_PLAYING:
                    DrawGame();
                    break;
                case MENU_STATE_PAUSED:
                    DrawGame();  // Draw game in background
                    DrawPauseMenu();
                    break;
                default: break;
            }
        EndDrawing();
    }
}
```

### 5.7 Input Mapping and Configurations

For a more flexible input system, it's a good practice to map physical inputs to game actions.

```cpp
// Define game actions
typedef enum {
    ACTION_MOVE_LEFT,
    ACTION_MOVE_RIGHT,
    ACTION_JUMP,
    ACTION_ATTACK,
    ACTION_INTERACT,
    ACTION_TOTAL  // Used to determine array size
} GameAction;

// Input configuration
struct {
    int keyboardKey;  // Keyboard key for this action
    int gamepadButton;  // Gamepad button for this action
} inputMap[ACTION_TOTAL];

// Initialize default controls
void InitInputMap() {
    inputMap[ACTION_MOVE_LEFT].keyboardKey = KEY_LEFT;
    inputMap[ACTION_MOVE_LEFT].gamepadButton = GAMEPAD_BUTTON_LEFT_FACE_LEFT;
    
    inputMap[ACTION_MOVE_RIGHT].keyboardKey = KEY_RIGHT;
    inputMap[ACTION_MOVE_RIGHT].gamepadButton = GAMEPAD_BUTTON_LEFT_FACE_RIGHT;
    
    inputMap[ACTION_JUMP].keyboardKey = KEY_SPACE;
    inputMap[ACTION_JUMP].gamepadButton = GAMEPAD_BUTTON_RIGHT_FACE_DOWN;
    
    inputMap[ACTION_ATTACK].keyboardKey = KEY_Z;
    inputMap[ACTION_ATTACK].gamepadButton = GAMEPAD_BUTTON_RIGHT_FACE_RIGHT;
    
    inputMap[ACTION_INTERACT].keyboardKey = KEY_E;
    inputMap[ACTION_INTERACT].gamepadButton = GAMEPAD_BUTTON_RIGHT_FACE_UP;
}

// Check if an action is being performed
bool IsActionPressed(GameAction action) {
    return IsKeyPressed(inputMap[action].keyboardKey) || 
           (IsGamepadAvailable(0) && IsGamepadButtonPressed(0, inputMap[action].gamepadButton));
}

bool IsActionDown(GameAction action) {
    return IsKeyDown(inputMap[action].keyboardKey) || 
           (IsGamepadAvailable(0) && IsGamepadButtonDown(0, inputMap[action].gamepadButton));
}

// Use in game code
if (IsActionDown(ACTION_MOVE_RIGHT)) {
    player.position.x += player.speed * GetFrameTime();
}

if (IsActionPressed(ACTION_JUMP)) {
    player.Jump();
}
```

### 5.8 Chapter Summary

- User input is fundamental to interactive game experiences
- Raylib provides comprehensive input handling for various devices
- Different input states (pressed, down, released) serve different gameplay needs
- Touch and gamepad support extends games to multiple platforms
- A well-designed menu system enhances user experience
- Input mapping creates a flexible control system that can be customized

### 5.9 Exercises

1. Create a program that visualizes all input states (show keys/buttons as they're pressed)
2. Implement a control remapping screen where users can change key bindings
3. Create a virtual on-screen joystick for touch devices
4. Design a menu system with animated transitions between different screens
5. Implement a system that combines multiple input types (e.g., keyboard + mouse)

### 5.10 Challenge Project: Input Showcase

Create an input demonstration program that:
- Shows real-time visualization of keyboard, mouse, and gamepad input
- Allows testing of different input combinations
- Includes a simple character that responds to input
- Provides a control remapping interface
- Saves and loads user preferences for controls
