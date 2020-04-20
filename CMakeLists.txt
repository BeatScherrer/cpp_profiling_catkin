cmake_minimum_required(VERSION 2.8.3)
project(cpp_profiling_catkin)

find_package(catkin_simple REQUIRED)

catkin_simple()

find_package(cpp_profiling CONFIG REQUIRED)

# get include dirs
get_target_property(CPP_PROFILING_INCLUDES cpp_profiling::cpp_profiling INTERFACE_INCLUDE_DIRECTORIES)

cs_export(
  INCLUDE_DIRS
    ${CPP_PROFILING_INCLUDES}
  LIBRARIES
    cpp_profiling::cpp_profiling
)
