cmake_minimum_required(VERSION 3.9.2)

if (MSVC)
	add_compile_options(/W4)
else()
	add_compile_options(-Wall -Wextra -Wpedantic --std=c++17) 
endif()

add_compile_options(-Wall -Wextra -Wpedantic --std=c++17) 

add_executable(intro main.cpp)
target_compile_features(intro PRIVATE cxx_lambda_init_captures)

