cmake_minimum_required(VERSION 3.20)
project(IDASignatureScanner)

set(CMAKE_CXX_STANDARD 23)

set(CMAKE_POSITION_INDEPENDENT_CODE ON)

add_library(IDASignatureScanner Source/IDASignatureScanner.cpp)
target_include_directories(IDASignatureScanner PUBLIC include)

add_executable(IDASignatureScannerMain Example/Main.cpp)
target_link_libraries(IDASignatureScannerMain PUBLIC IDASignatureScanner)
