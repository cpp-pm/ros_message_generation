cmake_minimum_required(VERSION 2.8.3)

include(cmake/HunterGate.cmake)
HunterGate(
  URL "https://github.com/ruslo/hunter/archive/v0.20.60.tar.gz"
  SHA1 "35a23a3e2f8a2c87f6762c43f3cc64a0bee50943"
)

project(message_generation)

hunter_add_package(catkin)
hunter_add_package(ros_gencpp)
hunter_add_package(ros_geneus)
hunter_add_package(ros_gennodejs)
hunter_add_package(ros_genlisp)
hunter_add_package(ros_genmsg)
hunter_add_package(ros_genpy)

find_package(catkin REQUIRED)

catkin_package(CATKIN_DEPENDS gencpp geneus gennodejs genlisp genmsg genpy)
