# RPG-CPP

RPG-CPP is a terminal-based role-playing game written in C++. This repository
contains a rebuild of the original project focused on portable, multiplatform
development and a consistent CMake-based build process.

## Features

- Character creation with selectable race, clothing, and starting location
- Exploration, combat, equipment, progression, and property management
- Colored terminal output and screen handling
- C++17 implementation
- CMake build configuration for Windows, macOS, and Linux

## Requirements

- A C++17-compatible compiler
- CMake 3.14 or newer
- A terminal with ANSI color and escape-sequence support

Supported toolchains include:

- GCC or Clang on Linux
- Apple Clang on macOS
- MSVC on Windows

## Building

### Using CMake

From the repository root, configure and build the project:

```bash
cmake -S . -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build
```

The executable is created at `build/program` on Unix-like systems and
`build/program.exe` on Windows.

Run the game with:

```bash
./build/program
```

On Windows, run `build\program.exe` from Command Prompt or PowerShell.

### Using the helper script

On macOS or Linux, the included script configures the project when necessary,
builds it, and starts the game:

```bash
./run.sh
```

To start the program under LLDB in debug mode:

```bash
./run.sh debug
```

The script is intended for Unix-like systems. On Windows, use the CMake
commands above with a supported generator.

## Project structure

```text
.
├── CMakeLists.txt   # Cross-platform CMake configuration
├── run.sh           # Build and run helper for macOS and Linux
└── src/
    └── main.cpp     # Game implementation
```

## Multiplatform rebuild

The project is being rebuilt from its previous platform-specific form to make
development and compilation consistent across operating systems. CMake is used
as the common build system, while platform-specific console initialization is
isolated behind conditional compilation where required.

The rebuild is an ongoing effort. Additional platform testing, code
organization, and gameplay improvements may be introduced over time.

## Contributing

Contributions and suggestions are welcome. When submitting changes, please
keep the code compatible with C++17 and verify that the project builds on the
platform you are targeting.

## License

This project is distributed under the MIT License. See the [LICENSE](LICENSE)
file for the complete license text.
