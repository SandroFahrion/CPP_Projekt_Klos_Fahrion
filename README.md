# CPP_Projekt_Klos_Fahrion
# How to run this program
## 1. Open a terminal in the project directory (where the main.cpp is located) and run:

```cmake -S . -B build```

```cmake --build build```

```
└── 📁CPP_Projekt_Klos_Fahrion
    └── .gitignore
    └── CMakeLists.txt
    └── 📁data
    └── 📁include
        └── bounding_box.hpp
        └── 📁game_mode
            └── game_mode.hpp
            └── mode_1_direct_click.hpp
            └── mode_2_color_change.hpp
        └── gui.hpp
        └── image.hpp
        └── kitti_dataset.hpp
        └── player.hpp
        └── reaction_game.hpp
    └── main.cpp
    └── README.md
    └── 📁src
        └── bounding_box.cpp
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