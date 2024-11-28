cmake_minimum_required(VERSION 3.4...3.14)
project(YAML_CPP VERSION 0.8.0 LANGUAGES CXX)


file(GLOB YAML_CPP_SRC
    "src/*.c"
    "src/*.cpp"
    "src/contrib/*.c"
    "src/contrib/*.cpp"
    )

add_library(YAML_CPP STATIC ${YAML_CPP_SRC})

add_compile_definitions(YAML_CPP_STATIC_DEFINE)

target_include_directories(YAML_CPP PUBLIC
    "include"
)

export(TARGETS YAML_CPP FILE YAML_CPP_CONFIG.cmake)
