cmake_minimum_required(VERSION 2.8.3)
project(mav_msgs)

find_package(catkin REQUIRED COMPONENTS
  std_msgs
  message_generation
)

add_message_files(
  FILES
  AttitudeCommand.msg
  Height.msg
  Status.msg
)

add_service_files(
  FILES
  GetMotorsOnOff.srv
  SetMotorsOnOff.srv
)

generate_messages(
  DEPENDENCIES std_msgs
)

catkin_package(
  CATKIN_DEPENDS std_msgs message_runtime
  )
