CMAKE_MINIMUM_REQUIRED(VERSION 2.6)
SET(PROJECTNAME torsoDemo)
PROJECT(${PROJECTNAME})

find_package(ICUB)
list(APPEND CMAKE_MODULE_PATH ${ICUB_MODULE_PATH})

include_directories(${YARP_INCLUDE_DIRS} ${ICUB_INCLUDE_DIRS})
add_executable(${PROJECTNAME} torsoDemo.cpp)
target_link_libraries(${PROJECTNAME} icubmod ctrlLib ${YARP_LIBRARIES})
install(TARGETS ${PROJECTNAME} DESTINATION bin)

