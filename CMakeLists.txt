cmake_minimum_required(VERSION 3.5.0)
project(CoopCode VERSION 0.1.0 LANGUAGES C CXX)

set(EXECUTABLE_OUTPUT_PATH ${CMAKE_CURRENT_SOURCE_DIR}/bin)

file(GLOB SOURCES "src/*.cpp")
add_executable(${PROJECT_NAME} main.cpp ${SOURCES})

target_include_directories(${PROJECT_NAME} PRIVATE ./include)
target_link_directories(${PROJECT_NAME} PRIVATE ./lib)

target_link_libraries(${PROJECT_NAME} PRIVATE SFUI_GOOGLELIKE)
target_link_libraries(${PROJECT_NAME} PRIVATE SFUI)
target_link_libraries(${PROJECT_NAME} PRIVATE sfml-graphics sfml-window sfml-system)

