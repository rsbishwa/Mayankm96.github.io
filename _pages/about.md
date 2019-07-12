---
layout: About
permalink: /
title: <strong>Bishwa Ranjan Si</strong>
description: Post Graduate Engineer Trainee | Sterlite Technologies

profile:
  align: left
  image: prof_pic.jpg
  address: #mention address

news: true
social: true
years: [2018]
---

I am currently working as a Post Grraduate Engineer Trainee in [Sterlite Technologies](https://www.sterlitetech.com/). 

I recently graduated from [IIT Kanpur](http://www.iitk.ac.in/) in June 2019 with a Masters and Bachelors(dual) in Chemical Engineering. During my Masters, I worked with [Prof. Rahul Mangal](http://home.iitk.ac.in/~mangalr/) on Active colloids.

Apart from my academics, I like reading novels(fantasy,thrillers) and watching documentaries of important events and about important people.
<div class="post">

  {% if page.news %}
    {% include news.html %}
  {% endif %}

</div>

---

## __publications__

{% for y in page.years %}
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

---

## __projects__

{% for project in site.projects %}

{% if project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="_blank">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

<div class="project ">
    <div class="thumbnail">
        <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %}

### other relevant projects

* Verification of Neural Networks using Linear Programming ([report](RIAI_Manuel_Mayank))
* Monocular Odometry with Bundle Adjustment ([report](/assets/documents/projects/VA4MR_Mini_Project.pdf), [video](https://www.youtube.com/watch?v=trbBh8Rjc4s&feature=youtu.be), [code](https://github.com/Mayankm96/Mono-Odometry))
* Survey on Variational Autoencoders for Bayesian Inference ([report](/assets/documents/projects/cs698-report.pdf))
* Visual Odometry using careful Feature Selection and Tracking ([report](/assets/documents/projects/ee698-report.pdf), [code](https://github.com/Mayankm96/Stereo-Odometry-SOFT))
* MATLAB based GUI for Motion Planning ([code](https://github.com/Mayankm96/Motion-Planning-GUI))
* Failure Handling in Swarm of Quadrotors ([report](/assets/documents/projects/cs637-report.pdf))

### open source projects

* ROS package for AirSim simulator- in C++ ([code](https://github.com/Mayankm96/airsim_img_publisher))
* ROS package for AirSim simulator- in Python ([code](https://github.com/Mayankm96/airsim_ros_client))
* ROS package for saving data published from Zed Camera ([code](https://github.com/Mayankm96/extract_zed_data))
* ROS package for publishing data from Sparton AHRS8 sensor ([code](https://github.com/Mayankm96/sparton_ahrs8_driver))

---

## __teaching__

* (Winter 2017: TA, guest lecturer): [AE640A: Autonomous Navigation](https://ae640a.github.io) with [Mangal Kothari](https://www.iitk.ac.in/aero/mangal/)

    * preparing course materials and assignments
    * guest lecturer on system integration using ROS ([slides](/assets/documents/teaching/ae640a/ae640a_lecture1.pdf)), robot simulation using Gazebo ([slides](/assets/documents/teaching/ae640a/ae640a_lecture2.pdf)), mathematical foundation for Robotics ([slides](/assets/documents/teaching/ae640a/ae640a_lecture9.pdf)), and non-parametric filters for localization

### tutorials

* (Spring 2019): Hierarchical Reinforcement Learning ([slides](/assets/documents/talks/HRL_Part2_Mayank.pdf))
* (Summer 2018): Introduction to Robot Operating System ([slides](/assets/documents/talks/Intro_to_ROS.pdf), [tutorial](/assets/documents/talks/Tutorial-ROS.pdf), [post](/blog/2017/ros-tips/))
* (Fall 2016): Sensors and Actuators ([slides](/assets/documents/talks/sensors-and-actuators.pdf))
* (Fall 2016): Introduction to Robotics ([slides](/assets/documents/talks/intro-to-robotics.pdf))
