cmake_minimum_required( VERSION 3.5 )

project(succotash)

file(GLOB SOURCES "${CMAKE_SOURCE_DIR}/src/*.cpp")

add_executable(${PROJECT_NAME} ${SOURCES})

target_include_directories(${PROJECT_NAME} PRIVATE "${CMAKE_SOURCE_DIR}/include")

add_subdirectory(dependencies/raylib)
target_link_libraries(${PROJECT_NAME} raylib)