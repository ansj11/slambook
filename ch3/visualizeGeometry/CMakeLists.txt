cmake_minimum_required( VERSION 3.0 )
project( visualizeGeometry )

set(CMAKE_CXX_FLAGS "-std=c++11")

# 添加Eigen头文件
include_directories( /usr/local/Cellar/eigen/3.4.0_1/include/eigen3 )

# 添加Pangolin依赖
find_package( Pangolin )
# message( ${Pangolin_INCLUDE_DIRS} )

include_directories( ${Pangolin_INCLUDE_DIRS} )

add_executable( visualizeGeometry visualizeGeometry.cpp )
target_link_libraries( visualizeGeometry ${Pangolin_LIBRARIES} )
