cmake_minimum_required(VERSION 2.8.3)
project(ros2_gazebo_test)

find_package(catkin REQUIRED)

catkin_package()

catkin_install_python(PROGRAMS
                      src/tf_republisher
                      src/map_republisher
                      DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})

install(FILES
  launch/test.launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
