FROM osrf/ros:humble-desktop



# RUN source /opt/ros/humble/setup.bash
# RUN mkdir -p ~/ros_WS
# WORKDIR ~/ros_WS
RUN mkdir -p /ros_WS/src
COPY /src /ros_WS/src
WORKDIR /ros_WS
RUN colcon build
COPY entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]