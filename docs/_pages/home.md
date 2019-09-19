---
layout: splash
permalink: /
header:
  overlay_color: "#5e616c"
  overlay_image: /assets/images/cover/test_header_shear_3.png
  actions:
    - label: "<i class='fas fa-download'></i> Install now"
      url: "/installation/"
excerpt: 
  Use camViz tool
feature_row:

  - image_path: /assets/images/cover/cover_column_3.png
    alt: "100% free"
    title: "More information"
    excerpt: "Find out more about the requirements and objectives of the project."
    url: "/about/"
    btn_class: "btn--primary"
    btn_label: "Learn more"   
youTube_id: foRCjyJFGI4
---

{% include feature_row %}


## What is CamViz?

This is a visualization tool, concerned with the client side. CamViz takes image from Pubisher, sends it to GUI (it has it’s own Gtk based GUI), and displays the continous stream of images. It can be used to take images from USB-cam as well as camera attached on a Robot.

<img src="/assets/images/camvizdocs.png" width="60%" height="40%">

Currently this tool is available in two branches:

1. ROS1 

It can be run used with Cameras and systems using ROS1 as middleware. To see how to use this tool visit the Installation and use page from the navigation bar.

2. ROS2 and ROS1

This branch provides an interface to run visualtize images with ROS1 as well as ROS2 from the same camViz tool. Instructions to run this version can be accessed by ROS2 release in the navigation bar. 

Please watch the video below to see how to run this tool.

{% include video id= "foRCjyJFGI4" provider="youtube" %}
