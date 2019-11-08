cmake_minimum_required(VERSION 3.13)
project(clion_opencv_tutorials4)

set(CMAKE_CXX_STANDARD 11)

set(OpenCV_DIR "C:\\opencv-build\\opencv-3.4.7-qt\\install")
find_package(OpenCV REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})

add_executable(clion_opencv_app main.cpp)
ADD_EXECUTABLE( main ./gui/main.cpp )
ADD_EXECUTABLE( ch3_sample1 ./gui/sample1.cpp )
ADD_EXECUTABLE( ch3_sample2 ./gui/sample2.cpp )
ADD_EXECUTABLE( ch3_sample3 ./gui/sample3.cpp )
ADD_EXECUTABLE( ch3_sample4 ./gui/sample4.cpp )
ADD_EXECUTABLE( ch3_sample5 ./gui/sample5.cpp )


target_link_libraries(clion_opencv_app ${OpenCV_LIBS})
TARGET_LINK_LIBRARIES( main ${OpenCV_LIBS} )
TARGET_LINK_LIBRARIES( ch3_sample1 ${OpenCV_LIBS} )
TARGET_LINK_LIBRARIES( ch3_sample2 ${OpenCV_LIBS} )
TARGET_LINK_LIBRARIES( ch3_sample3 ${OpenCV_LIBS} )
TARGET_LINK_LIBRARIES( ch3_sample4 ${OpenCV_LIBS} )
TARGET_LINK_LIBRARIES( ch3_sample5 ${OpenCV_LIBS} )
