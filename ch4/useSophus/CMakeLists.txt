cmake_minimum_required( VERSION 3.0 )
project( useSophus )

include_directories( /usr/local/Cellar/eigen/3.4.0_1/include/eigen3 )

# 为使用 sophus，您需要使用find_package命令找到它
find_package( Sophus REQUIRED )
include_directories( ${Sophus_INCLUDE_DIRS} )

add_executable( useSophus useSophus.cpp )
target_link_libraries( useSophus ${Sophus_LIBRARIES} )
