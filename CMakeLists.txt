cmake_minimum_required(VERSION 3.13)
project(clion_opencv_tutorials4)

set(CMAKE_CXX_STANDARD 11)

set(OpenCV_DIR "C:\\opencv-build\\opencv-3.4.7-qt\\install")
find_package(OpenCV REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})

add_executable(clion_opencv_app main.cpp)
ADD_EXECUTABLE( sample1 ./basic/sample1.cpp )
ADD_EXECUTABLE( sample2 ./basic/sample2.cpp )
ADD_EXECUTABLE( sample3 ./basic/sample3.cpp )


target_link_libraries(clion_opencv_app ${OpenCV_LIBS})
TARGET_LINK_LIBRARIES( sample1 ${OpenCV_LIBS} )
TARGET_LINK_LIBRARIES( sample2 ${OpenCV_LIBS} )
TARGET_LINK_LIBRARIES( sample3 ${OpenCV_LIBS} )
