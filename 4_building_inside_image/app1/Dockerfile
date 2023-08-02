FROM osrf/ros:humble-desktop


#voir https://roboticseabass.com/2023/07/09/updated-guide-docker-and-ros2/
ARG ROS_DISTRO=humble
ENV ROS_DISTRO=${ROS_DISTRO}
SHELL ["/bin/bash", "-c"]



# RUN source /opt/ros/humble/setup.bash
# RUN mkdir -p ~/ros_WS
# WORKDIR ~/ros_WS
RUN mkdir -p /ros_WS/src
COPY /src /ros_WS/src
WORKDIR /ros_WS
RUN source /opt/ros/humble/setup.bash && colcon build
COPY entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]