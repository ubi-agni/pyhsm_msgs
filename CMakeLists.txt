cmake_minimum_required(VERSION 3.10.2)
project(pyhsm_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation std_msgs)

add_message_files(FILES
  HsmStructure.msg
  HsmState.msg
  HsmTransition.msg
  HsmCurrentState.msg
)

generate_messages(DEPENDENCIES std_msgs)

catkin_package(CATKIN_DEPENDS message_runtime)
