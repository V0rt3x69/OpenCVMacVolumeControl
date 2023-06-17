cmake_minimum_required(VERSION 3.23)
project(OpenCVProjectVolume)

set(CMAKE_CXX_STANDARD 14)


set(OpenCV_DIR "/usr/local/Cellar/opencv/4.7.0/share/OpenCV")
find_package(OpenCV REQUIRED)


set(SOURCE_FILES main.cpp)
add_executable(OpenCVProjectVolume main.cpp)


target_link_libraries(OpenCVProjectVolume ${OpenCV_LIBS})

target_link_libraries(OpenCVProjectVolume "-framework CoreAudio")

