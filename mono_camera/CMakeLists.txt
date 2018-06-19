project(Camera_Calibration)
cmake_minimum_required(VERSION 2.8)

#check opencv_version: pkg-config --modversion opencv 
#set(OpenCV_DIR "/usr/local/opencv3.2.0/share/OpenCV")
find_package(OpenCV 2.4.13 REQUIRED HINTS /home/zc/tools/opencv-2.4.13/share/OpenCV)

include_directories(${OpenCV_INCLUDE_DIR})
#add_executable(Camera_Calibration camera_calibration.cpp)
add_executable(Camera_Calibration cali.cpp)
target_link_libraries(Camera_Calibration ${OpenCV_LIBS})

