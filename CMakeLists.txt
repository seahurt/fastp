cmake_minimum_required(VERSION 3.16)
project(fastp)

file(GLOB SRC_FILES ${PROJECT_SOURCE_DIR}/src/*.cpp )

link_directories(${PROJECT_SOURCE_DIR}/lib64)

add_executable(fastp ${SRC_FILES} )
target_link_libraries(fastp -static -Wl,--no-as-needed -pthread -lpthread -lisal -ldeflate )



