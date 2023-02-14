cmake_minimum_required(VERSION 3.5)

project(isaac_ros_apriltag_interfaces)

find_package(
  catkin
  REQUIRED
  COMPONENTS geometry_msgs
             message_generation
             std_msgs
  )

add_message_files(
  FILES AprilTagDetection.msg
        AprilTagDetectionArray.msg
  )

generate_messages(
  DEPENDENCIES std_msgs
               geometry_msgs
  )

catkin_package()
