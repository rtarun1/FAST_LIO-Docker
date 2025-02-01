FROM ghcr.io/rtarun1/fast_lio_base:latest

# Add the following labels
LABEL org.opencontainers.image.description="ROS2 Development Container for FAST-LIO"
LABEL org.opencontainers.image.title="ROS2FAST-LIO"
LABEL org.opencontainers.image.vendor="Tarun R"
LABEL org.opencontainers.image.source="https://github.com/rtarun1/DockerForROS2Development"
LABEL maintainer="tarun.ramak@gmail.com"
LABEL org.opencontainers.image.licenses="MIT"

COPY . /home/rtarun1/ros2_ws/src

WORKDIR /home/rtarun1/ros2_ws
# handle default shell
SHELL ["/bin/bash", "-c"]
RUN source /opt/ros/humble/setup.bash \
    && colcon build \
    && source install/setup.bash 
