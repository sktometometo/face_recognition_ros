cmake_minimum_required(VERSION 3.0.2)
project(face_recognition_ros)

find_package(catkin REQUIRED COMPONENTS catkin_virtualenv)

catkin_python_setup()

catkin_generate_virtualenv(
  PYTHON_INTERPRETER python3
  USE_SYSTEM_PACKAGES FALSE
  CHECK_VENV FALSE
)

catkin_package(
)

catkin_install_python(
  PROGRAMS
    scripts/face_classifier.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
