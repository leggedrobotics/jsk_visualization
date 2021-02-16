cmake_minimum_required(VERSION 3.1)
project(jsk_rviz_plugins_msgs)

set(PACKAGE_DEPENDENCIES
  message_generation
  geometry_msgs
  std_msgs
)

find_package(catkin REQUIRED
  COMPONENTS
    ${PACKAGE_DEPENDENCIES}
)


# Declare the service, message and action files to be built
add_message_files(FILES
  OverlayText.msg
  OverlayMenu.msg
  TransformableMarkerOperate.msg
  ObjectFitCommand.msg
  Pictogram.msg
  PictogramArray.msg
  RecordCommand.msg
  StringStamped.msg
)

add_service_files(FILES
  EusCommand.srv
  Screenshot.srv
)

generate_messages(
  DEPENDENCIES
    geometry_msgs
    std_msgs
)

catkin_package(
  CATKIN_DEPENDS
    ${PACKAGE_DEPENDENCIES}
)
