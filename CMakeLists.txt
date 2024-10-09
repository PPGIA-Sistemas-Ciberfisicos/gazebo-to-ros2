cmake_minimum_required(VERSION 3.5)

project(gazebo_gz_to_ros2_simples)

find_package(ament_cmake REQUIRED)

# Install project launch files
install(
  DIRECTORY
    launch/
  DESTINATION share/${PROJECT_NAME}/launch
)

# Install project configuration files
install(
  DIRECTORY
    config/
  DESTINATION share/${PROJECT_NAME}/config
)

install(
  DIRECTORY
    gz_sim/models/
  DESTINATION share/${PROJECT_NAME}/gz_sim/models
)

install(
  DIRECTORY
    gz_sim/worlds/
  DESTINATION share/${PROJECT_NAME}/gz_sim/worlds
)

install(
  PROGRAMS
    scripts/Pose_to_tf
  DESTINATION lib/${PROJECT_NAME}
)


if(BUILD_TESTING)
  find_package(ament_lint_auto REQUIRED)
  ament_lint_auto_find_test_dependencies()
endif()


ament_environment_hooks("${CMAKE_CURRENT_SOURCE_DIR}/hooks/${PROJECT_NAME}.dsv.in")
ament_package()
