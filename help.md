# Computer Graphics Lab 2 - Repository Guide

## 📚 Project Overview

This repository contains **Lab 2** for the course **INF01047 - Computação Gráfica e Visualização I** (Computer Graphics and Visualization I) at UFRGS (Universidade Federal do Rio Grande do Sul), taught by Prof. Eduardo Gastal.

### Project Title: "Coelinhos do Brasil" (Rabbits of Brazil)

The task is to create a 3D graphics program that renders a specific scene as shown in the reference video (`resultado-esperado.mp4`).

## 📂 Directory Structure

### `cg-lab2/` Contents

#### 📋 Documentation Files
- **`README.md`** - Main instructions and project overview
- **`TAREFAS.md`** - Task description (reproduce the video result)
- **`CHECKLIST.md`** - Verification checklist for completion
- **`RELATORIO.md`** - Lab report template (to be filled by student)
- **`COMPILACAO.md`** - Compilation instructions for different platforms
- **`COMPILACAO.md`** - Report documenting implementation

#### 🛠️ Build System
- **`CMakeLists.txt`** - CMake configuration (recommended for Linux)
- **`CMakePresets.json`** - CMake build presets
- **`Makefile`** - Build file for Linux/macOS
- **`Makefile.macOS`** - macOS-specific build configuration

#### 📦 Source Code (`src/`)
- **`main.cpp`** - Main application entry point
  - Sets up OpenGL context using GLAD and GLFW
  - Loads 3D models from OBJ files using TinyObjLoader
  - Handles rendering loop and user input
  
- **`shader_vertex.glsl`** - Vertex shader program (GPU code for vertex processing)
- **`shader_fragment.glsl`** - Fragment shader program (GPU code for pixel coloring)
- **`textrendering.cpp`** - Utilities for rendering text on screen
- **`buildtriangles.cpp`** - Functions to build triangle meshes
- **`correcao.cpp`** - Additional correction/utility functions
- **`glad.c`** - GLAD implementation (OpenGL loader)
- **`tiny_obj_loader.cpp`** - OBJ file format loader implementation

#### 📚 Headers (`include/`)
- **`utils.h`** - Utility functions and helpers
- **`matrices.h`** - Matrix operation utilities
- **`dejavufont.h`** - Font data for text rendering
- **`tiny_obj_loader.h`** - OBJ loader header
- **OpenGL Headers:**
  - `glad/glad.h` - OpenGL function pointers
  - `GLFW/` - Window and input handling library
  - `KHR/` - Khronos standard headers

- **GLM Headers (`glm/`)** - Mathematics library for graphics
  - Vector types: `vec2.hpp`, `vec3.hpp`, `vec4.hpp`
  - Matrix types: `mat2x2.hpp` through `mat4x4.hpp`
  - Mathematical functions (trigonometric, exponential, geometric, etc.)

#### 📦 Libraries (`lib-*/`)
Pre-compiled libraries for different platforms:
- `lib-linux/` - Linux libraries
- `lib-mingw-32/` - MinGW 32-bit (Windows)
- `lib-mingw-64/` - MinGW 64-bit (Windows)
- `lib-ucrt-64/` - Windows UCRT (Universal C Runtime)
- `lib-vc2022/` - Visual C++ 2022 (Windows)

#### 📦 Data (`data/`)
- Contains model files (`.obj`), textures, and other assets needed by the program

## 🔧 Key Technologies

| Technology | Purpose |
|-----------|---------|
| **C++** | Main programming language |
| **OpenGL 3.3+** | Graphics API (via GLAD) |
| **GLFW 3** | Window creation and input handling |
| **GLM** | Mathematics library for vectors/matrices |
| **GLSL** | Shader programming language |
| **TinyObjLoader** | Load 3D models in OBJ format |
| **CMake** | Build system (recommended) |

## 🚀 Compilation

The project supports multiple compilation methods:

### Option 1: CMake (Recommended)
```bash
cmake --workflow --preset configure-build-run
```

This automatically:
1. Creates and configures a build directory
2. Compiles the project
3. Executes the compiled program

### Option 2: Make (Linux/macOS)
```bash
make           # Compile
make run       # Run the program
make clean     # Clean build artifacts
```

### Option 3: Windows (Visual Studio)
Use the pre-built library in `lib-vc2022/` with Visual Studio project configuration.

## 📝 Tasks

### Task 1: Reproduce Expected Output
- Modify the C++ source code to render the scene shown in `resultado-esperado.mp4`
- Update the window title to format: `INF01047 - [Your Student ID] - [Your Full Name]`
- The program is evaluated based on how closely it matches the reference video

## ✅ Completion Checklist

Before submitting:
1. Review [CHECKLIST.md](cg-lab2/CHECKLIST.md) for all required elements
2. Fill out [RELATORIO.md](cg-lab2/RELATORIO.md) with your implementation report
3. Verify the window title has correct format
4. Test that output matches the reference video

## ⚠️ Important Rules

- **AI Usage**: You can use AI tools freely, **except for writing the final report**
- **Collaboration**: You can discuss ideas with classmates, but **NO file sharing** (code, images, prompts, etc.)
- **Do NOT modify**: `README.md` and `TAREFAS.md` to avoid conflicts with professor updates

## 📖 Development Tips

1. **Shader Programming**: Modify shaders in `shader_vertex.glsl` and `shader_fragment.glsl` to change visual appearance
2. **Model Loading**: Load new models by adding lines in `main.cpp` using ObjModel class
3. **Transformations**: Use GLM functions (in headers) to create rotation, scaling, and translation matrices
4. **Debugging**: Use `printf()` statements in C++ to debug rendering issues

## 🔗 References

- [Wavefront OBJ Format](https://en.wikipedia.org/wiki/Wavefront_.obj_file)
- [GLM Documentation](https://glm.g-truc.net/)
- [OpenGL Tutorial](https://learnopengl.com/)
- [TinyObjLoader](https://github.com/syoyo/tinyobjloader)

---

**Created**: Lab 2 for INF01047 at UFRGS  
**Language**: C++  
**Graphics API**: OpenGL 3.3+
