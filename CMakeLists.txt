cmake_minimum_required(VERSION 2.8.3)
project(bag_to_images)

find_package(catkin REQUIRED)

catkin_package()

#catkin_python_setup()

include_directories(${catkin_INCLUDE_DIRS})
include_directories(include ${catkin_INCLUDE_DIRS})

SET(PY_PROJECT_NAME bag_to_images)
SET(PY_PACKAGE_DIR python)

install(DIRECTORY python/
        DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
        USE_SOURCE_PERMISSIONS
        PATTERN ".svn" EXCLUDE)
