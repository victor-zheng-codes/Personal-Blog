---
title: "Robotics Blogs"
date: 2023-12-03T15:18:04-05:00
draft: false
author: "Victor Zheng"
showToc: true
tags: ["robotics"]
categories: [""]
TocOpen: true
hidemeta: false
comments: false
description: "From 2018 to 2021, I was part of a robotics team which I had the chance of writing blogs about"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: "https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/robotics_2019.jpg?raw=true" # image path/url
    alt: "Picture of robot from TFA Juniors Robotics" # alt text
    caption: "One of our robots for RoboCup Junior Maze" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/victor-zheng-codes/Personal-Blog/tree/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

From 2018 to 2021, I was a part of "The Future Academy Robotics" Juniors Robotics team out in Vancouver, Canada. 

We were a team of high-school students operating 3-5 days a week after-school, working on building autonomous robots to tackle some of the robotics problems of our world. We competed in mainly RoboCup Junior Maze and Soccer, which involved designing, building, prototyping, and testing autonomous robots that would compete against other robots at international competitions. 

We competed in National tournaments and International tournaments. In particular, the best experience for me was an event held in Sydney, Australia in 2019 for RoboCup Junior 2019. 

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/firefighting%20awards.jpg?raw=true)|
| :--: |
| <b>RoboRave Firefighting in 2019 in Albuquerque, New Mexico</b>|

I was part of teams from 2018 to 2021, with achievements including: 

2021
* RoboCup Junior International, Soccer, 1st Place (February)
* RoboCup Junior International, Rescue, 2nd Place (July)

2020
* RoboCup Junior International, Rescue, 1st Place (October)
* RoboCup Junior West Canada, Rescue, 2nd Place (February)

2019
* RoboRave North America, Fire Fighting, 1st Place (May)
* RoboCup Junior International, Super Team Maze, 2nd Place (July)

2018
* RoboCup Junior Canada West, Rescue, 1st Place (December)

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/firefighting.jpg?raw=true)|
| :--: |
| <b>RoboRave Firefighting in 2019 in Albuquerque, New Mexico</b>|



## The following are blogs that I wrote while on the team

----
### Making a reliable Computer Vision Letter Detection Algorithm (Oct 7, 2023)

In the [RoboCup Rescue Simulation Demo Competition](https://rescue.rcj.cloud/), a reliable visual victim finding algorithm is crucial for success. Each successful victim identification can be worth 40 points, which can add up to be the difference between first and second. Our victim identification algorithm was created through OpenCV, by designing an algorithm capable of differentiating between H, S, and U. We looked at the key points in each letter, and from there, looked to differentiate each key point from each letter from one another.

After preprocessing, the first step in this process was looking at the middle to top pixel area, and determining the number of contours in this region. If the number of contours was greater than or equal to 3, then we could already say that this is an S. If the crop is 0, then we can say that this is a U. We continued differentiating key points until we were left with a letter as a result.

This algorithm process can be seen through the decision tree below:

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/letter%20detection%20algo.png?raw=true)|
| :--: |
| <b>Letter detection algorithm</b>|


By being able to test our program through the display function, we were able to determine whether or not our algorithm works. We were able to easily fix any issues, and perform with higher accuracy. 

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/world1_3.png?raw=true)|
| :--: |
| <b>Finding the letter U accurately</b>|



----

### Testing Image Processing Algorithms in a Webots World (Sep 23, 2020)

In the 2020 [RoboCup Junior Simulation Demonstration Competition](https://rescue.rcj.cloud/), one of the objectives is to differentiate between letters using Computer Vision. A correct identification gains bonus points, and every point can matter in the event. In the past, our team had used OpenCV’s built-in functions to draw lines, shapes, and text onto images. However, we found that this was difficult to do on the Webot’s simulation platform. This posed a challenge for testing our vision systems.

Our team tried testing images without writing looking at the testing areas, but the errors made it difficult to know what was going on in the image. We knew that we needed to solve this problem.

Therefore, we researched Webots and found a device called [Webot’s Display](https://cyberbotics.com/doc/reference/display). We immediately researched how to use it and found that we could simply add it to our .wbt world file. We then attached the Display to our Webots world file, and voila, we could use it to test!

Our team managed to attach the camera image to the display, and then write onto the image using the width and x/y coordinates. This made testing much, much more easier.

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/world1_2.png?raw=true)|
| :--: |
| <b>Example of simulated image detection</b>|


----

### Data Visualization in Webots world (Sep 16, 2020)

Creating a robust and reliable robot is an important part of the RoboCup Rescue Simulation Demonstration Competition. When testing in Webots, our team used Data Visualization to determine how/when errors occurred. Each time we tested our robot, we wrote data from sensors such as colour, gyro, and gps into a file. Then, we used the data to find the key points and see how/what caused the errors. These errors could then be examined for strategy errors, coding errors, or noise errors. We could then create a more reliable and robust robot, since there were less challenges that could affect our robot.

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/data-visualization.JPG?raw=true)|
| :--: |
| <b>Data visualization example for RoboCup Junior Simulation</b>|


----

### RCJ Rescue Simulation Noise Researching (Sep 14, 2020)

During the [RoboCup Junior Rescue Simulation Demonstration Competition](https://rescue.rcj.cloud/events/2020/simulation/index.html), our team performed many tests, one of which was to find noise. David from our team, developed many worlds for us to test. We then performed Data Visualization on the data, to find unique aspects or occurrences. During our research, we found that the noise in the Webots Simulation Platform is very limited. We sometimes however, got errors such as “World Timestep Errors”, which we could not find reasons for. However, we found that the probability of this error of occurring spiked when the robot was moving in repetitive motions or volatilely.

Our team tried avoiding these errors by ensuring complete movements, and testing, testing testing.

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/competition_5.png?raw=true)|
| :--: |
| <b>Example of simulated image detection</b>|

----
