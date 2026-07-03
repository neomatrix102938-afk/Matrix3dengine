Markdown

# 3D Console Wireframe Render Engine

A lightweight, from-scratch 3D wireframe graphics engine built entirely in C# that renders 3D geometry inside a standard text terminal console using ASCII/ANSI characters.

## Features

- **Pure Software Renderer:** No heavy graphics libraries (like OpenGL or DirectX)—built using pure mathematical vertex projection.
- **Dynamic 3D Camera:** Move around the sandbox world using `W`, `A`, `S`, `D` and use the arrow keys or mouse tracking to look around in 3D space.
- **Physics System:** Built-in jump physics and basic gravity simulation (`Spacebar`).
- **Auto-Centering OBJ Parser:** Automatically parses and centers standard custom low-poly `.obj` files to sit perfectly on the map workspace layout.
- **Live Terminal HUD:** Displays live player coordinates (`XYZ`) and status indicators.
- **Integrated Terminal Chat/Command Input:** Press `Enter` to access a command line console window natively inside the application runtime.

## Controls

| Key | Action |
| --- | --- |
| **W / S** | Move Forward / Backward |
| **A / D** | Strafe Left / Right |
| **Arrow Keys** | Look Up / Down / Left / Right |
| **Spacebar** | Jump |
| **Enter** | Open/Close Terminal Chat & Commands Line |

### Commands
* `/tp spawn` or `/kill` - Teleports your camera matrix instantly back to the core spawn block.
* `/tp <X> <Y> <Z>` - Teleports the camera to exact coordinates.

## How to Run

1. Make sure you have the [.NET SDK](https://dotnet.microsoft.com/download) installed.
2. Clone or download this project folder.
3. Open your terminal in the project directory and run:
   ```bash
   dotnet run

Custom 3D Models

To load your own custom geometry, place an untextured low-poly .obj file inside the root directory and name it model.obj.

    ⚠️ Important: To maintain a smooth frame rate in the terminal window, make sure your custom .obj file is a low-poly asset and under 2 MB in size. Files with too many polygons will slow down the real-time render loop.

The engine's built-in parser will automatically normalize its bounds math, center it, and draw it on screen alongside the default spawn structures!
