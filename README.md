# Cub3d

_Cub3d_ is a School 42 project focused on building a basic 3D game engine using raycasting techniques. In this project, you will implement a simple 3D renderer in C that simulates a 3D perspective on a 2D grid map. The project challenges you to work with graphics programming, input handling, and basic game mechanics, while also enhancing your understanding of low-level programming and mathematical concepts.

---

## Table of Contents

- [Introduction](#introduction)
- [Project Description](#project-description)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [Author](#author)
- [License](#license)

---

## Introduction

The _Cub3d_ project is a hands-on challenge designed to introduce you to 3D game engine development using raycasting. Inspired by early 3D games like Wolfenstein 3D, this project focuses on rendering a 3D world from a 2D map, handling user inputs, and managing basic collision and navigation mechanics.

---

## Project Description

In Cub3d, you will develop a 3D engine that:
- Uses raycasting to simulate a 3D environment on a 2D grid-based map.
- Renders walls, floors, ceilings, and sprites based on a given map configuration.
- Handles player movement, collision detection, and basic game mechanics.
- Supports simple textures for walls and objects to enhance visual realism.

The project is structured to break down the main functionalities into modules, such as:
- **Map Parsing:** Reading and validating the map configuration.
- **Raycasting Engine:** Calculating ray intersections and rendering the scene.
- **User Input:** Managing keyboard and mouse inputs for player control.
- **Game Loop:** Continuously updating the game state and rendering frames.

---

## Features

- **Raycasting Engine:** Implements raycasting techniques to render a 3D view from a 2D map.
- **Texture Mapping:** Applies textures to walls and sprites to give a realistic appearance.
- **User Control:** Supports keyboard inputs for navigation and interaction within the game.
- **Optimized Rendering:** Designed for efficiency while maintaining simplicity in design.
- **Modular Design:** Separated into modules to enhance readability and maintainability.

---

## Prerequisites

Ensure you have the following installed before building the project:
- A C compiler (such as `gcc`)
- [Make](https://www.gnu.org/software/make/) for build automation
- The [MiniLibX](https://harm-smits.github.io/42libs/) graphics library, as required by the project
- A Unix/Linux development environment or equivalent (such as macOS with proper setup)
- Basic knowledge of C programming and graphics programming concepts

---

## Installation

Follow these steps to clone, build, and run Cub3d on your machine:

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/Kinglo25/Cub3d.git
   cd Cub3d
   ```

2. **Build the Project:**

   Clean up any previous builds and compile the project using Make:

   ```bash
   make fclean
   make
   ```

3. **Verify the Build:**

   Run the executable to check that the engine starts correctly:

   ```bash
   ./Cub3d maps/your_map_file.cub
   ```

   Replace `maps/your_map_file.cub` with the path to a valid map file.

---

## Configuration

The Cub3d engine relies on a configuration file (with a `.cub` extension) that contains the map layout and texture paths. A typical configuration file includes:

- **Map Layout:** A grid representing walls, spaces, and sprites.
- **Texture Paths:** File paths for wall textures, sprite textures, and any additional graphics.
- **Player Settings:** Initial coordinates and viewing direction for the player.

Example snippet from a configuration file:

```ini
NO ./textures/wall_north.xpm
SO ./textures/wall_south.xpm
WE ./textures/wall_west.xpm
EA ./textures/wall_east.xpm

# Map layout
1111111111
1000000001
1011001101
1000000001
1111111111
```

Ensure that paths and map data are correctly configured for your setup.

---

## Usage

After building the project, start the engine with a map file:

```bash
./Cub3d maps/your_map_file.cub
```

- **Controls:**  
  - Use the arrow keys or `W`, `A`, `S`, `D` for movement.
  - Rotate the view with the left/right arrow keys.
  - Use additional keys as defined by your implementation (refer to your project documentation).

- **Game Loop:**  
  The program will continuously render the 3D environment based on the player's input until the window is closed.

---

## Troubleshooting

- **Compilation Issues:**  
  Ensure that all prerequisites, including MiniLibX, are correctly installed and configured.  
  Double-check your Makefile settings if errors occur during build.

- **Runtime Errors:**  
  Verify that the provided map file exists and is correctly formatted.  
  Check that texture file paths are correct and that MiniLibX is properly linked.

- **Graphics Issues:**  
  If the screen does not display correctly, ensure your graphics environment supports MiniLibX and that your drivers are up to date.

For additional troubleshooting, consult project documentation, your peers, or instructors at School 42.

---

## Contributing

Contributions to Cub3d are welcome! To contribute:
1. Fork the repository.
2. Create a new branch for your changes (`git checkout -b feature/my-feature`).
3. Make your modifications and ensure code follows the School 42 guidelines.
4. Commit your changes with clear messages.
5. Push your branch and create a pull request for review.

Your input and improvements help enhance the project for the entire community.

---

## Author

- **Kinglo25**  
  [GitHub: Kinglo25](https://github.com/Kinglo25)

Developed as part of the School 42 curriculum.

---

## License

Distributed under the MIT License. See the `LICENSE` file for more details.
```

---

This README file is ready to use for the Cub3d project on GitHub. Simply update any specific details (such as paths or control schemes) if needed, and enjoy sharing your project!
