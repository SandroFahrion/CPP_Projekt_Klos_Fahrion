# CPP_Projekt_Klos_Fahrion
## How to use
### Prerequisites
1. **CMake**: Install the latest version of CMake.
2. **Compiler**: Ensure an appropriate compiler is installed:
   - **Windows**: Visual Studio or MinGW.
   - **Linux**: GCC.
3. **OpenCV Source Code**: OpenCV from [GitHub](https://github.com/opencv/opencv).

### Installing OpenCV
1. **Clone OpenCV repository into the project workspace:**
```
└── KITTI_Reaction_Game_workspace (example)
    └── 📁KittiReactionGame_Projekt
        └── 📁CPP_Projekt_Klos_Fahrion
            └── ...
    └── 📁opencv
        └── ...
```
2. **Set up build directory**:
Open a command terminal in ```opencv``` and run
```
mkdir build && cd build
```
3. **Configure CMake**:
   Run the appropriate CMake command based on your platform and compiler:

   - **General (Recommended: automatic compiler detection)**:
     ```bash
     cmake -S .. -B .
     ```

   - **Visual Studio**:
     ```bash
     cmake -G "Visual Studio 17 2022" -A x64 -S .. -B .
     ```

   - **MinGW**:
     ```bash
     cmake -G "MinGW Makefiles" -S .. -B .
     ```

4. **Start the build**:
   Run the build command:
     ```bash
     cmake --build .
     ```

5. **Installation**:
   After a successful build, you can install the libraries:
   ```bash
   cmake --install .
    ```
### Build KittiReactionGame
Open a command terminal in ```CPP_Projekt_Klos_Fahrion``` and run
```
cmake -S . -B build`
```

```
cmake --build build
```

### Launch KittiReactionGame
Open a terminal in ```build/Debug``` and run

```
KITTIReactionGame.exe
```

### (Optional) Build and Launch with Debugging Mode
1. **To build:** Open a command terminal in ```CPP_Projekt_Klos_Fahrion``` and run
```
cmake -S . -B build_debug -DENABLE_DEBUG=ON
```
2. **To launch:**
Open the terminal in ```build_debug/Debug``` and run

```
KITTIReactionGame.exe --debug
```

## Full Workspace Structure
**After setting everything up, your workspace should look like this:**

```
└── 📁KittiReactionGame_Projekt
    └── 📁opencv
        └── 📁build
        └── ...
    └── 📁CPP_Projekt_Klos_Fahrion
        └── .gitignore
        └── CMakeLists.txt
        └── 📁data
            └── 📁data_tracking_image_2
                └── 📁testing
                    └── 📁image_02
                        └── 📁0000
                            └── 000000.png
                            └── 000001.png
                            └── ...
            └── 📁data_tracking_label_2
                └── 📁training
                    └── 📁label_02
                        └── 0000.txt
                        └── 0001.txt
                        └── ...
        └── 📁helpers
            └── member_util.hpp
        └── 📁include
            └── bounding_box.hpp
            └── debug.hpp
            └── debug.tpp
            └── 📁game_mode
                └── game_mode.hpp
                └── mode_1_direct_click.hpp
                └── mode_2_color_change.hpp
            └── gui.hpp
            └── image.hpp
            └── kitti_dataset.hpp
            └── player.hpp
            └── reaction_game.hpp
            └── serialize.hpp
        └── main.cpp
        └── README.md
        └── 📁src
            └── bounding_box.cpp
            └── debug.cpp
            └── 📁game_mode
                └── game_mode.cpp
                └── mode_1_direct_click.cpp
                └── mode_2_color_change.cpp
            └── gui.cpp
            └── image.cpp
            └── kitti_dataset.cpp
            └── player.cpp
            └── reaction_game.cpp
        └── 📁test
            └── CMakeLists.txt
```