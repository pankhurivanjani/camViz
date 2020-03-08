---
permalink: /installation/
title: "Installation and use"

sidebar:
  nav: "docs"

toc: true
toc_label: "TOC installation"
toc_icon: "cog"
---



## Ubuntu/Debian

The programming environment is composed of the (a) ROS1 middleware, and (b) JdeRobot base. All this software is open source so there are alternative ways to install all of them directly from the source code. Currently we use ROS Melodic,  and JdeRobot-base (2018-06-06) releases.

### Prerequisites

First check that you have the following dependencies installed. If not, you can install them in the links provided.

- Ubuntu 18.04 

- JdeRobot base (Not necessary)

- ROS(Robot Operating System)

- OpenCV

- Download github Desktop <a href="https://desktop.github.com" target="_blank">from here</a>.



### Installation
Follow the next steps to have the environment up and running, ready to use.

Branch 1: To run this tool with ROS1 

1. Install ROS framework.

    Add the lastest ROS sources:

    ```bash
    sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
    ```

    ```bash
    sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116
    ```
    
2. Install colcon

    ```bash
    sudo apt install python3-colcon-common-extensions
    ```

3. Install the packages.

    ```bash
    sudo apt-get install ros-melodic-desktop-full
    ```

4. Install the JdeRobot-Academy software

    Once you have JdeRobot installed in your system, you can download and install the Academy software. To do so, you must:

    ```bash
    git clone https://github.com/JdeRobot/.git

    sudo apt install jderobot-gazebo-assets

    ```

5. Install CamViz tool

- Clone CamViz - repository.

    Download the Academy software. With git Shell clone the repository as in Linux and run the exercices with `CMD` o powershell

    ```bash
    git clone https://github.com/JdeRobot/camViz.git
    ```

_Note: Github repositories are located in `Documents\GitHub`_


### Run CamViz

Branch 1: ROS1

- Terminal 1

   ```roscore```

- Terminal 2

Run any image publisher in ROS

Ex: ```rosrun usb_cam usb_cam_node```

- Terminal 3

    ```bash
    cd camViz
    ```
    ```bash
    colcon build
    ```
    ```bash
    source /opt/ros/melodic/setup.bash
    ```
    ```bash
    cd build/jderobot_camviz 

    ./camViz camViz.yml
    ```

You can watch a video demonstration in the home page.
