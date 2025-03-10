Project Cub3D - 42 School
The Cub3D project is a captivating dive into computer graphics and game development at 42 School, inspired by the classic Wolfenstein 3D. Students create a 3D maze game using raycasting to render a first-person perspective from a 2D map. This project teaches fundamentals of real-time rendering, event handling, and low-level graphics programming while emphasizing performance and precision.
Core Objective

Develop a dynamic 3D maze explorer that renders a navigable environment from a user-defined map file. The program must parse map configurations, handle player movement, and display textured walls, floors, and ceilings in real time using raycasting techniques.
Key Requirements

    Map Parsing:

        Read a .cub file defining:

            Textures for walls (North, South, East, West).

            Colors for floor and ceiling (RGB values).

            A 2D map grid (0 = empty, 1 = wall, N/S/E/W = player start).

        Validate the map:

            Must be enclosed by walls.

            No invalid characters or configuration errors.

    Rendering:

        Use raycasting to project a 3D view from the 2D map.

        Apply textures to walls and solid colors to floors/ceilings.

        Smoothly render movement and rotations (keyboard + mouse).

    Player Controls:

        WASD for movement.

        Arrow keys or mouse to rotate the camera.

        ESC to exit the game.

    Error Handling:

        Gracefully exit on invalid maps, missing textures, or incorrect RGB values.

        Prevent memory leaks and crashes.

Technical Implementation

    Raycasting Algorithm:

        Cast rays for each vertical screen column.

        Calculate ray direction, wall intersections, and distances.

        Determine wall height and texture coordinates for each "slice."

        Render floors/ceilings using horizontal distance calculations (bonus).

    Graphics Library:

        Use MinilibX (42's lightweight graphics library) for window management, pixel rendering, and event hooks.

    Map Validation:

        Flood-fill or BFS to ensure the map is fully enclosed.

        Check for valid player spawn points and forbidden characters.

    Event Loop:

        Handle keyboard/mouse inputs via MinilibX hooks (mlx_hook, mlx_loop_hook).

        Update player position and camera angles based on inputs.

        Implement collision detection to prevent walking through walls.

    Texture Management:

        Load textures from .xpm files into buffers.

        Map texture pixels to wall slices based on ray hit positions.

Bonus Extensions

Optional features to enhance gameplay and complexity:

    Minimap: Display a 2D overhead map in a corner.

    Sprite Rendering: Add static or animated objects (e.g., lamps, enemies).

    Door Mechanics: Open/close doors with a key press.

    Mouse Look: Rotate the view horizontally/vertically with mouse movement.

    Skybox: Render a dynamic sky texture or day/night cycle.

    Sound Effects: Play sounds for actions like walking or opening doors.

Learning Outcomes

    Raycasting: Understand how 3D projection is simulated using 2D math.

    Graphics Programming: Manipulate pixels, textures, and event loops with MinilibX.

    Game Physics: Implement movement, collision detection, and camera controls.

    File Parsing: Validate and process structured configuration files.

    Optimization: Balance rendering quality and performance for real-time updates.

Cub3D bridges creativity and technical rigor, offering hands-on experience in game development. It challenges students to combine mathematical precision with software design, resulting in a functional and immersive 3D engine. Mastery of this project lays the groundwork for advanced graphics programming and engine development.