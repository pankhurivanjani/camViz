---
permalink: /installationros2/
title: "ROS2 Release"

sidebar:
  nav: "docs"

toc: true
toc_label: "TOC installation"
toc_icon: "cog"
---



## Ubuntu/Debian

The programming environment is composed of the (a) ROS1 middleware, (b) ROS2 middleware and (c) JdeRobot base. All this software is open source so there are alternative ways to install all of them directly from the source code. Currently we use ROS Melodic, ROS Dashing and JdeRobot-base (2018-06-06) releases.

### Prerequisites

First check that you have the following dependencies installed. If not, you can install them in the links provided.

- Ubuntu 18.04 

- JdeRobot base 

- ROS(Robot Operating System) Melodic

- ROS2 Dashing

- OpenCV

- Download github Desktop <a href="https://desktop.github.com" target="_blank">from here</a>.



### Installation
Follow the next steps to have the environment up and running, ready to use.

**Switch to ROS-ROS2 interface branch

Branch 2: To run this tool with ROS2 and ROS1


1. Install ROS2 framework.

    Add the lastest ROS2 sources:

    ```bash
    sudo locale-gen en_US en_US.UTF-8
    sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
    export LANG=en_US.UTF-8
    ```

    ```bash
    sudo locale-gen en_US en_US.UTF-8
    sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
    export LANG=en_US.UTF-8
    ```
    ```bash
    sudo sh -c 'echo "deb [arch=amd64,arm64] http://packages.ros.org/ros2/ubuntu `lsb_release -cs` main" > /etc/apt/sources.list.d/ros2-latest.list'
    ```
    ```bash
    sudo apt update
    ```
    ```bash
    sudo apt install ros-dashing-desktop

    ```
    ```bash
    sudo apt install python3-argcomplete
    ```
    ```bash
    sudo apt update
    sudo apt install ros-dashing-rmw-opensplice-cpp # for OpenSplice
    sudo apt install ros-dashing-rmw-connext-cpp # for RTI Connext (requires license agreement)
    ```

2. Install ROS framework.

    Add the lastest ROS sources:

    ```bash
    sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
    ```
    ```bash
    sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116
    ```
    
3. Install colcon

    ```bash
    sudo apt install python3-colcon-common-extensions
    ```

4. Install the packages.

    Install the following packages:

    ```bash
    sudo apt-get install ros-melodic-desktop-full
    ```

5. Install the JdeRobot-Academy software

    Once you have JdeRobot installed in your system, you can download and install the Academy software. To do so, you must:

    ```bash
    git clone https://github.com/JdeRobot/base.git

    sudo apt install jderobot-gazebo-assets

    ```

6. Install CamViz tool

- Clone CamViz - repository.

    Download the Academy software. With git Shell clone the repository as in Linux and run the exercices with `CMD` o powershell

    ```bash
    git clone https://github.com/JdeRobot/camViz.git
    ```
    
_Note: Github repositories are located in `Documents\GitHub`_


### Run CamViz


Branch 2: ROS2 and ROS1

**Please Clean previous builds and caches from build, install and logs folder when moving from ROS1 to ROS2 or vice versa**

Case 1: ROS1

- Terminal 1

Run any image publisher in ROS

Ex: ```rosrun usb_cam usb_cam_node```

- Terminal 2

    ```bash
    cd camViz
    ```
    ```bash
    colcon build --symlink-install \--cmake-args \ -Drosversion:string=1
    ```
    ```bash
    source /opt/ros/melodic/setup.bash
    ```
    ```bash
    cd build/camViz 

    ./camViz camViz.yml
    ```
    
Case 2: ROS2

- Terminal 1

Run any image publisher in ROS

Ex: ``` Follow this github repo https://github.com/klintan/ros2_usb_camera ```

- Terminal 2

    ```bash
    cd camViz
    ```
    ```bash
    colcon build --symlink-install \--cmake-args \ -Drosversion:string=0
    ```
    ```bash
    source /opt/ros/dashing/setup.bash
    ```
    ```bash
    cd build/camViz 

    ./camViz camViz.yml
    ```
- Change User name in CMakeLists in path '/home/(username)...'


You can watch a video demonstration in the home page.



