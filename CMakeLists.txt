cmake_minimum_required(VERSION 3.4...3.14)
project(YAML_CPP VERSION 0.8.0 LANGUAGES CXX)

add_library(YAML_CPP STATIC)

target_sources(YAML_CPP PRIVATE
    "src/*.c"
    "src/*.cpp"
    "src/contrib/*.c"
    "src/contrib/*.cpp"
    )


add_compile_definitions(YAML_CPP_STATIC_DEFINE)

target_include_directories(yaml-cpp PUBLIC
    "include"
)

export(TARGETS YAML_CPP)
