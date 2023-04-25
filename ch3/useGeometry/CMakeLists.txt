cmake_minimum_required( VERSION 3.0 )
project( geometry )

# 添加Eigen头文件
# include_directories( "/usr/include/eigen3" )
include_directories( /usr/local/Cellar/eigen/3.4.0_1/include/eigen3 )

add_executable( eigenGeometry eigenGeometry.cpp )
