cmake_minimum_required(VERSION 3.16)
project(iai_icub_description)

# Required for ROS 2 packages
find_package(ament_cmake REQUIRED)

# If this package contains URDF/SDF files, add these dependencies:
find_package(ament_cmake REQUIRED)
find_package(urdf REQUIRED)          # For URDF support
find_package(sdformat_urdf REQUIRED) # For SDF support (if needed)

# Install URDF/SDF/meshes to share/${PROJECT_NAME}
install(
  DIRECTORY robots/iCubGazeboV3_visuomanip meshes
  DESTINATION share/${PROJECT_NAME}
)

# Declare as a ROS 2 package
ament_package()