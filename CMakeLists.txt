cmake_minimum_required(VERSION 2.8.3)
project(spatial_db_msgs)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  mesh_msgs
  geometry_msgs
  visualization_msgs
  message_generation
)

add_message_files(
  FILES
BoundingBox.msg
BoundingBoxStamped.msg
ColorCommand.msg
GeometryCollection.msg
LabelCommand.msg
LabeledBoundingBox.msg
LabeledGeometryCollection.msg
ObjectDescription.msg
ObjectInstance.msg
ObjectInstanceOverview.msg
OrientationBox.msg
Point2DModel.msg
Point3DModel.msg
Polygon2DModel.msg
Polygon3DModel.msg
PolygonMesh3DModel.msg
PolygonMesh.msg
PolygonMeshStamped.msg
Pose2DModel.msg
Pose3DModel.msg
TriangleMesh3DModel.msg
)

generate_messages(
  DEPENDENCIES
  mesh_msgs geometry_msgs visualization_msgs
)

catkin_package(
  INCLUDE_DIRS
  CATKIN_DEPENDS
    roscpp
    mesh_msgs
    geometry_msgs
    visualization_msgs
)
