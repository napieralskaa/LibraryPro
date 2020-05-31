cmake_minimum_required(VERSION 3.10)
project(ppprojekt)

set(CMAKE_CXX_STANDARD 11)

add_subdirectory(
        ${CMAKE_CURRENT_LIST_DIR}/SQLiteCpp
)

include_directories(
        ${CMAKE_CURRENT_LIST_DIR}/SQLiteCpp/include
)

add_executable(ppprojekt src/main.cpp)

target_link_libraries(ppprojekt
        SQLiteCpp
        sqlite3
        pthread
        dl
        )