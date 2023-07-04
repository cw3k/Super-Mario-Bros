cmake_minimum_required(VERSION 3.25)
project(super_mario_kofybrek)

set(CMAKE_CXX_STANDARD 17)

include_directories(Source/Headers)

add_executable(super_mario_kofybrek
        Source/Headers/Animation.hpp
        Source/Headers/ConvertSketch.hpp
        Source/Headers/DrawMap.hpp
        Source/Headers/Enemy.hpp
        Source/Headers/Global.hpp
        Source/Headers/Goomba.hpp
        Source/Headers/Koopa.hpp
        Source/Headers/MapCollision.hpp
        Source/Headers/MapManager.hpp
        Source/Headers/Mario.hpp
        Source/Headers/Mushroom.hpp
        Source/Animation.cpp
        Source/ConvertSketch.cpp
        Source/DrawMap.cpp
        Source/Enemy.cpp
        Source/Goomba.cpp
        Source/Koopa.cpp
        Source/Main.cpp
        Source/MapCollision.cpp
        Source/MapManager.cpp
        Source/Mario.cpp
        Source/Mushroom.cpp)

include(FetchContent)
FetchContent_Declare(SFML
        GIT_REPOSITORY https://github.com/SFML/SFML.git
        GIT_TAG 2.6.x)
FetchContent_MakeAvailable(SFML)

target_link_libraries(super_mario_kofybrek PRIVATE sfml-graphics sfml-window sfml-system sfml-audio)