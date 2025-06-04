add_library(mod_graphics mod_graphics.cpp)

# Create an alias for the module (namespace-style)
add_library(C++GameEngine::mod_graphics ALIAS mod_graphics)

# Include directories for public headers
target_include_directories(mod_graphics
  ${WARNING_GUARD}
  PUBLIC
    $<BUILD_INTERFACE:${PROJECT_SOURCE_DIR}/include>
    $<BUILD_INTERFACE:${PROJECT_BINARY_DIR}/include>
)

# Set C++ standard
target_compile_features(mod_graphics PUBLIC cxx_std_20)

# Set target properties
set_target_properties(mod_graphics PROPERTIES
  VERSION ${PROJECT_VERSION}
  CXX_VISIBILITY_PRESET hidden
  VISIBILITY_INLINES_HIDDEN YES
)
