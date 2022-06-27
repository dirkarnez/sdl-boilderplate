cmake_minimum_required(VERSION 3.14)

project(sdl2-boilerplate)

# set(CMAKE_CXX_STANDARD 11)
# set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(SDL2 REQUIRED PATHS "${SDL_ROOT}")

SET(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} -static")

add_executable(${PROJECT_NAME}
    "src/main.cpp"
)

target_link_libraries(${PROJECT_NAME} mingw32 SDL2::SDL2main SDL2::SDL2-static)