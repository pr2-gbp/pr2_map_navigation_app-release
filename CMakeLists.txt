cmake_minimum_required(VERSION 2.8.3)
project(pr2_map_navigation_app)
find_package(catkin REQUIRED COMPONENTS pr2_position_scripts pr2_navigation_teleop pr2_navigation_perception amcl pr2_machine pr2_navigation_global pr2_navigation_config tf topic_tools map_store)

#generate_messages(
#    #TODO DEPENDENCIES geometry_msgs std_msgs
#)

catkin_package(
    DEPENDS pr2_position_scripts pr2_navigation_teleop pr2_navigation_perception amcl pr2_machine pr2_navigation_global pr2_navigation_config tf mongodb topic_tools map_store
    CATKIN_DEPENDS # TODO
    INCLUDE_DIRS # TODO include
    LIBRARIES # TODO
)

install(FILES amcl_node.xml map_nav.app map_nav.interface map_nav.launch pr2_2dnav.launch map.jpg DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
