cmake_minimum_required(VERSION 2.8.3)
project(laas_navigation)

find_package(catkin REQUIRED COMPONENTS
)

catkin_package(
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

# install
foreach(dir launch maps morse_pepper_launch morse_pepper_move_base_config morse_pr2_launch morse_pr2_move_base_config pr2_launch pr2_move_base_config rviz scripts)
   install(DIRECTORY ${dir}/
      DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/${dir})
endforeach(dir)
