add_subdirectory(mod_graphics)

add_executable(C++GameEngine main.cpp engine.cpp)
target_link_libraries(C++GameEngine PRIVATE C++GameEngine::mod_graphics)
