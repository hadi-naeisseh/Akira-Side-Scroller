cmake_minimum_required(VERSION 3.10)

project(AkiraSideScroller)

# Set C++ standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Add SDL2
#set(SDL2_DIR "C:\projects\Akira-Side-Scroller\include\SDL2")
#set(SDL2_TTF_DIR "path_to_your_SDL2_ttf_directory")

# Include SDL2
find_package(SDL2 REQUIRED)
#find_package(SDL2_ttf REQUIRED)

include_directories(${SDL2_INCLUDE_DIRS} )#${SDL2_TTF_INCLUDE_DIRS})

# Add source files
add_executable(AkiraSideScroller src/main.cpp src/Game.cpp)

# Link SDL2 libraries
target_link_libraries(AkiraSideScroller ${SDL2_LIBRARIES}) #${SDL2_TTF_LIBRARIES})
