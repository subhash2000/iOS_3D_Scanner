cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

project(3d_pcl_scan)

find_package(PCL 1.3 REQUIRED COMPONENTS common io)

include_directories(${PCL_INCLUDE_DIRS})


link_directories(${PCL_LIBRARY_DIRS})

add_definitions(${PCL_DEFINITIONS})
add_executable(pcd_write_test pcd_write.cpp)
add_executable (resampling_test resampling.cpp)
target_link_libraries(pcd_write_test ${PCL_LIBRARIES})
target_link_libraries (resampling_test ${PCL_LIBRARIES})