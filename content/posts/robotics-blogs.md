---
title: "Robotics Blogs"
date: 2023-12-03T15:18:04-05:00
draft: false
author: "Victor Zheng"
showToc: true
tags: ["robotics"]
categories: ["robotics"]
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

NOTE: These blogs were previously posted at: https://rcj.tfacademy.ca/ and some content referenced may no longer exist

----
### Heated Victim Detection using Vision in RCJ Maze Simulation (Mar 26, 2021)

Heated victim detection is one of the things that the TFA Junior Robotics Team intends to explore following the 2020 RCJ Rescue Demonstration Competition. The team had previously used vision to detect only visual victims. Although the rules have not been released yet, the TFA Junior Robotics Team is keen on getting a head start, and honing their image processing skills.

By detecting a red circle, the TFA Junior Robotics Team can possibly detect a heated victim from over a few tiles away. This is because the side facing heat sensors can not detect victims facing forward. However the cameras are in the front, which enables a direct view of approaching heated victims. By implementing this type of strategy, the TFA Junior Robotics Team has the advantage of being able to detect victims in a more optimized way. The team can optimize their mapping algorithm and optimize their time in the maze by reaching victims faster. 

The original plan was in reading an image and using OpenCV to detect the red circles. However, after applying a mask, the results were unexpected.  This can be seen in the image below.


|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/unexpected.JPG?raw=true)|
| :--: |
| <b>Unexpected result of finding red values<b>|

After realizing that the results were unexpected, the team investigated the situation. The first thing that the TFA Junior Robotics Team attempted was in writing out the image array into a new image. In the above image, you can see the new image after reading the image data. One can also see that the team tested their process on the Windows photo app.  

The new image was all dark, and seemed to only have 1 channel. Therefore, the team went back to the drawing board. From there, the team brainstormed and determined that they should attempt to read the image array data into another file. This took many attempts, as seen in the photos below…

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/mixed-up-channels.JPG?raw=true)|
| :--: |
| <b>Reading the image into a new file<b>|

After correcting the colour, the team found that the image was upside down. Therefore, the team created an algorithm to flip the image data across the centre line. The result was a righted image as shown below. 

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/recorrected.JPG?raw=true)|
| :--: |
| <b>Flipping the image<b>|

As seen in the above photo, the team proceeded to display the image via the display function. The team did this by reading the file that was previously written by the Pillow Library.  

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/proceeding_to_test_images.png?raw=true)|
| :--: |
| <b>Here we began to display the image using the display function<b>|


Following this, the team proceeded to begin creating and testing a mask. Through writing a mask algorithm that detected the highest and lowest thresholds for the red mask, the team was able to slightly detect the red image. 

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/red-detection-in-the-RoboCUp.png?raw=true)|
| :--: |
| <b>Red detection with a mask<b>|

From there, the team played around with both the output and the algorithm to see which methods would find the red the best. 

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/masked_result.png?raw=true)|
| :--: |
| <b>Masked result after all filtering<b>|

The end result was an algorithm that found the red pixels and displayed them onto a mask. This proved that it was possible to detect colours in the RCJ Rescue Simulation Demonstration Platform. 

UPDATE: As of March 28, 2021, there seems to be no heated victims in future competitions. However, this algorithm may be used in detecting the new hazard signs. The new rules can be found here.

Here is a close up of the red detection and the resulting mask.


|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/original_to_new.png?raw=true)|
| :--: |
| <b>Original to new at the end<b>|

----
### Future Image Processing in the RoboCup Junior Maze Simulation World (Mar 20, 2021)

After competing in the RoboCup Junior Rescue Simulation Demonstration Competition in 2020, the TFA Junior Robotics Team realized that there were still many improvements to be made going forward.

The vision component of the RCJ Rescue Maze Simulation consists of the visual victim detection, along with other detection algorithms. The TFA Junior Robotics team was very successful with Image Processing during the 2020 RoboCup Junior Rescue Simulation Demonstration Competition. However, even with a 100% success rate in victim detection, the team knows that there is a lot to improve on. Improvements include, 1. increasing the speed of visual victim detection, 2. detecting other objects in the world, and 3. improving the accuracy.

The following are some methods that the TFA Junior Robotics Team has analyzed to potentially use in the future. 

**Object detection**

This idea involves finding other objects in the field. This objects could include obstacles, walls, checkpoints, swamps, and/or black holes. By detecting other objects in the field, the TFA team is able to optimize scoring and therefore, score more points. The team is also able to use the camera as a way to cross check with other sensors, and therefore, improve the robustness of the robot. 


|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/object_detection.png?raw=true)|
| :--: |
| <b>Object detection algorithms?<b>|


**Using C instead of Python**

Another possible implementation would be using C instead of Python to increase processing speed for use on algorithms on an embedded systems in the future. Previously, the TFA Junior Robotics had intended to test the team’s algorithms through the Webots Display, however, the team is now leaning towards writing it’s code through image processing algorithms in C, and extending it to python. This allows the team to possibly not use the OpenCV library, and develop a specialized library for the team itself. It also allows the team to embed image processing algorithms into other devices, in a post pandemic world. 

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/obstacle1H.png?raw=true)|
| :--: |
| <b>Better letter detection algorithms?<b>|

**Red Capturing**

Something that the TFA Junior Robotics Team attempted during the RCJ Rescue Simulation Demonstration Competition was in detecting the red circles indicating heated victims. Since the placement of the heat sensors were on the sides of the robot, the team thought that they could try detecting heated victims in the front using the three front facing cameras.

If the team is able to do this, then they can possibly be able to head straight towards the heated victim instead of detecting it when the heat sensors do. This results in a faster run, as the victim detection is optimized with more victims “rescued” at a faster pace. 

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/red-capturing-wall.png?raw=true)|
| :--: |
| <b>Red capturing algorithms?<b>|


**Machine Learning or Dynamic Weighted or Adaptive Letters Tree**

Something else that that the TFA Junior Robotics team thought of implementing was a machine learning, dynamically weighted, or adaptive weighting for visual victim detection. Currently, TFA’s victim detection is a long list of “if” statements, but if the team can implement a dynamically weighted algorithm, then it is possible to improve this system. 

Essentially, by arranging a points or reward system for each victim detection, the robot can decide which letter is more probable. This can possibly improve the overall victim detection accuracy and robustness.

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/dynamic-weighting-robot.png?raw=true)|
| :--: |
| <b>Using weighted algorithms?<b>|


**BMP images in Webots world**

Previously, the TFA Junior Robotics Team had also studied BMP image conversion. There is a possibility that the team implements this in the near future. This enables to team to not use the OpenCV library, and instead, design algorithms specific to the needs of the competition. This idea could be an extension of writing in C programming language, or could be done through Python.

Another possibly would be in completely getting rid of images, and instead using the color channels that make up an image. This would mean that there would be no need for BMP images nor OpenCV in the team’s image processing algorithms. 

----
### Dynamic Weighted Algorithms in RoboCup Junior Simulation Soccer (Mar 14, 2021)

Dynamically Weighted algorithms may be one of the future steps that TFA Junior Robotics Team takes in the upcoming June 2021 RCJ Competition.

This idea involves having numerous different strategies, techniques, or algorithms, and applying a dynamic weight. For example, if an algorithm is successful in scoring a goal, then perhaps the weight of this algorithm increases. In essence, a good dynamically weighted algorithm will find the best strategy against opponents, resulting in a better chance at scoring the further the match plays out. In other words, a dynamic weighted algorithm will help teams improve robustness by adapting to scenarios on the fly. The TFA Junior Robotics Team may decide to use dynamic algorithms at the next iteration of events.

**What is the reward?**

The dynamic relationship between multiple variables takes a long time to create, and can be arduous at first. However, a proper dynamic weighted algorithm can result in in lots of success, as the opponent’s weakness is exploited. A team can reap the rewards of a problem in the opposing team’s code, and score the max amount of goals. In addition, a team can adapt to different teams, against numerous different strategies and techniques. For instance, a static algorithm would not adapt to every single opponent in the world, whereas a dynamic algorithm would. Therefore, a team can ensure that they are prepared for any challenge posed by any team.

**What are the drawbacks?**

There are of course, some drawbacks to a dynamically weighted algorithm.

If a dynamically weighted algorithm ends up having a small flaw, one can easily get beaten in all of one’s matches. For example, if there is one weight that turns out to be flawed, then one risks the entire algorithm failing.

Another drawback would be the time necessary for a Dynamic Algorithm to be implemented. In a match, there are only 10 minutes, so without enough trials, one risks using inaccurate or inconsistent results. This could also cause issues if the weight does not have enough time to generate the most accurate result. A 45 minute match would result in a more accurate dynamically weighted algorithm than one in 10 minutes.

Finally, one risks getting lucky sometimes instead of actually winning. For instance, if one adds “points” or weight to a flawed algorithm thanks to an own-goal or something that a dynamic algorithm did not control, then the algorithm can be falsely correct. This can result in a “false-positive” type of result, with inaccurate, and ultimately incorrect dynamic weight. As a type of Monte Carlo method, it is essential that the data one collects fits a pattern, and is not totally random and incomputable.

**What are the next steps?**

The TFA Junior Robotics Team is currently consolidating their strategies and determining the viability of pursuing and creating a dynamically weighted algorithm.


|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/Dynamic_Adaptive-Weighting-1.png?raw=true)|
| :--: |
| <b>Dynamic weighted algorithms? This is soemthing we discussed.<b>|

----
### TFA Junior Robotics Ball Handling Strategies (Mar 2, 2021)

In the RoboCup Soccer Simulation World, ball acceleration and deceleration are two topics that the TFA Junior Robotics Team looked into. Ball acceleration and deceleration can affect the entire ball prediction algorithm. Without an accurate ball prediction strategy, one risks going to the wrong predicted position and losing or not winning control of the ball.

The TFA Junior Robotics Team hypothesizes that the deceleration is affected by the mass and the force that the ball enters the wall. Under review, one can find that the ball does not always come back from the wall in the same direction. This was found by determining what happens at the collision by doing a close inspection of the ball and the location that it lands. The TFA Junior Robotics Team hypothesises that ball will slow down by half, with a +- 0.001 offset for both the x and y values. This is not exact, but is an approximation of the exact acceleration/deceleration of the ball.

While going on a straight path, the ball will not slow down, unless acted upon by an external force. Once the ball touches the wall, some of its speed will slow, however the second timestep determines the actual change. Therefore, it is very challenging in implementing a change in between two timesteps. Therefore, this prediction will not be 100% accurate. 


**Why does the ball doesn’t come back in a straight path?**

The TFA Junior Robotics Team has also found that the ball does not come at a straight path after colliding with a wall. The team has considered the possibility that the wall is in fact not flat, and therefore, the ball prediction is not possible. Another possibility is that the ball rotation plays a factor, where the ball is rotating when hitting the wall. This causes the ball to spin at unforeseen angles. This is something that the TFA Junior Robotics team is actively trying to figure out. 

**Newton’s First Law in action**

As seen in this above video, the ball collides with a robot. This results in the ball gaining momentum from the collision and moving forward at a constant velocity. As seen in the above video, the ball continues on at a constant speed and separates from the chasing robot.

Unlike the ball in the field, this ball will not stop, as it is in an inertial field of motion. This proves that the Webots world maintains Newton’s First Law of Motion, and that there is no air resistance or friction in the world.

**Ball deceleration/acceleration analysis**

The TFA Junior Robotics Team found out about the Ball Acceleration and Deceleration topic when the team compared the predicted point of the ball and the actual point in the world. The team wrote the predicted data into files, and using data visualization, quickly graphed the predicted vs actual data. This resulted in a graph of the large discrepancy between the actual and the predicted point. Therefore, the team chose to investigate this problem further. 

**Ball running inside the field**
As seen in the above video, the ball continues to go forward  unless acted on by an external force. This is correct according to Newton’s First Law of motion. Once the ball hits the wall, there is no longer an inertial frame of reference, where the ball is acted on a force by the wall. This causes the ball to lose it’s velocity, and therefore, slow down. Energy is likely transferred, and momentum from the collision results in a change in resulting velocity. Ultimately, due to the diminishing speed of the ball, the simulator supervisor calls Lack of Progress, and the ball is relocated to the centre.  

**Conclusion**
After studying the Webots world, the TFA Robotics Team concludes that there is no acceleration or deceleration of motion without an external force acting on the ball. This proves that the Webots world has no air resistance or friction. However, when inside the soccer field, the wall acts as a force when collided on with, and results in the ball slowing down.

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/acceleration-and-decelleartion.JPG?raw=true)|
| :--: |
| <b>Acceleration and deceleration of the ball is something that we considered when designing our automated robots<b>|


----
### TFA Junior Robotics Ball Handling Strategies (Mar 2, 2021)

In the RCJ Soccer Simulation world, TFA Junior Robotics has worked on creating cohesive ball handling strategies.

TFA’s algorithm involves two major parts, the ball prediction, and the directional thinking processes.

In ball prediction, TFA’s algorithm involves a complex ball prediction algorithm, which can be seen in our Ball Prediction post. In this, and the Ball Prediction along corner post, we talked about how we determined the future position of the ball.

In ball handling, we focused on creating an algorithm that could move the ball from the defending to attacking quickly. Our team developed an algorithm that would chase the ball in an indirect line to the predicted ball position. Instead, our team based our algorithm on a point or distance away from the ball. This resulted in our robots reaching the ball at the predicted point, but also being able control the ball in our intended position. For instance, our robots during the RoboCup Junior Soccer Simulation Demonstration Competition were able to direct the ball at the opponents goal even when defending in our own half. 

----
### Communication in the RCJ Soccer Simulation Communication (Feb 8, 2021)

In the RCJ Soccer Simulation world, communication is an essential part of working together and winning in the competition. Without a good communication algorithm or network, robots could be prone to being by themselves, knocking each other over, or duplicating on roles.

Therefore, the communication issue is one that TFA Junior Robotics team has taken very seriously.

One way that TFA thought they could manage communication was through the emitter/receiver devices that are embedded on the world. However, after careful inspection of the world files and provided supervisors, our team decided that this would not be possible.

The second way that TFA thought of managing the communication problem was through creating a server that could be connected to all the robots. However, due to the uncertainty of success, along with the uncertainty of rule permitted, our team also decided to forgo this idea.

This lead to our current idea, which is to not have robot to robot communication. Instead, our team decided to simply use the same code in each robot. By putting the same code in each robot, we ensure that they are all running using the same algorithm. This makes it easy to assign roles specific to the distances calculated through the GPS values.

Some of the things that each robot communicates with each other are: the distances to the ball, the distances to each other, the distances to the goal, and the distances to the center. These distances help our team decide whether to assign one or another role to each robot.

 
As you can see in this video, the distances provided by the GPS values create a unified and cohesive attack and defence for both sides. The provided GPS values are essentially a replacement for a communication system.

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/communicating.JPG?raw=true)|
| :--: |
| <b>Communication between robots is not an easy task<b>|

----

### RoboCup Junior Soccer Simulation Robot Wheels Falling Off (Jan 26, 2021)

While testing with Webot’s simulation soccer, we found that the wheels could fall off. This happens almost always with the demo player provided, and with robots that don’t have good movement control. We have found that this is one of the main problems that may occur in the simulation world, and are keen on avoiding it. Robots can get unplayable when this problem occurs, and can cause a huge problem in a team’s algorithm.

This is not a bug, but rather a good thing, since this shows how real the Webots simulator is.


2 ways that a wheel can fall off:
1. When the robot goes from a fast speed to a slow speed
2. When the robot is transported

One way of preventing a robot from moving from fast to slow is by creating a dead zone that prevents the motors from going back and forth over a large distance. Another method is in ensuring that the motor speeds never change rapidly by comparing the previous speed with the current speed.

These methods ensure that the motors never have to change speeds rapidly, resulting in wheels falling off. 

 
In the RCJ Soccer Simulation Demonstration rules, a Lack of Progress is defined as when “there is no progress in the gameplay for a reasonable period of time. Typical lack of progress situations are when the ball is stuck between robots, when there is no change in ball and robot’s positions, or when the ball is beyond detection or reach capability of all robots on the field.”

By detecting a lack of progress, a team is able to stop or alter it’s movement to prevent a wheel from moving while being transported.

Another way to prevent wheels from falling off from being transported is by stopping once our robot scores. This is because after a goal is scored, the robots are also relocated. 

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/wheels-falling-off.JPG?raw=true)|
| :--: |
| <b>We had  to deal with wheels falling off<b>|

----
### Ball Prediction Along a Corner (Jan 20, 2021)

In RCJ Soccer Simulation, the corner is a triangle that can change the angle of the ball moving. In a normal ball prediction algorithm, the ball will reflect along the x and y wall.

However, along a corner, the ball does not reflect along this wall, but rather at a pi/4 diagonal member. This 45 degree angled triangle can prove costly if the ball prediction algorithm does not take this into account. A robot’s ball prediction algorithm is automatically wrong when the ball approaches a corner, and thus, has less ball control. The Junior Robotics Team at TFA has looked into this problem, and found a way to detect the corner.

By detecting a corner, robots can achieve a better ball prediction algorithm and meet the ball up faster to score goals or defend better. In tight matches, a good corner ball prediction can mean the difference between a win and a loss. 

TFA Junior Robotics’ algorithm is to switch the x and y axis’. This is essentially the same as reflecting the ball at a diagonal point. However, there are intricacies with detecting when the ball will hit the corner. For this, there are a few ways to accomplish this, however, Victor made an algorithm by calculating if the given GPS point is inside the area of the triangle. Since the three corner points and the current ball position is given, a simple formula for calculating if a point is inside a triangle can be used. Therefore, the ball prediction knows

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/corner-ball-prediction.JPG?raw=true)|
| :--: |
| <b>Predicting where the simulated soccer ball will go after hitting a corner<b>|


----

### Why we gave up Machine Learning in RCJ Soccer Simulation Demo (Jan 5, 2021)

In the RoboCup Junior Soccer Simulation Competition, our team considered using Machine Learning and/or Reinforcement Learning in our algorithm.

However, there were some challenges that we considered:

* Time constraints
* Whether we could implement it
* Learning new concepts in less than one month
* Uncertainty of success

These challenges resulted in our team choosing not to attempt a machine learning/reinforcement learning algorithm for this competition.

----

### Soccer Simulation Ball Prediction (Dec 27, 2020)

An important part of the RoboCup Junior Soccer Simulation Demo Competition is the ball prediction. Our team used an algorithm involving finding the next x and y locations. We also found that Webot’s has deceleration when the ball hits a wall. This makes sense, as the ball is transferring force into the wall, and the speed decreases.

We look at the change in the x and y values, and determine where the ball will be in an x number of timesteps. This x number of timesteps can be altered according to the distance of the robot to the actual ball location.

By predicting the ball’s position, we are able to meet the ball faster, without spending time chasing the ball.

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/ball-prediction.JPG?raw=true)|
| :--: |
| <b>Ball prediction based off of the direction that the balls are currently heading in<b>|

----

### Designing a Dummy Goalie for Testing in RCJ Soccer (Dec 24, 2020)

One of the important features of testing offence programs in the RoboCup Soccer Simulation Demonstration Competition is having an opposing team that can defend. This makes it essential to have a goalie or defender for offensive players to test against. The TFA Junior Robotics team created a dummy player that could simply head towards a ball, and then turn back when the ball was out of range. This goalie can be improved in the future, however, it currently serves an important purpose of testing offensive programs against it.


As seen in the video, the robot heads back to an “origin” point before chasing the ball. The goalie makes a sort of semi-circle area that it can defend in. This ensures that the robot never leaves the goal, yet is also able to defend against balls coming near. This will also be improved on with the ball prediction algorithm that the team is working on right now. With both the ball prediction and the goalie added, the TFA Junior Robotics Team can start practicing their attacking robots. The TFA Junior Robotics Team believes that the attacking portion will be one of the more important and time consuming aspects, and thus, will be focusing lots of attention there as the competition nears. 

Note: video no longer exists

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/dummy-goalie.JPG?raw=true)|
| :--: |
| <b>One of the designs of our goalies for testing<b>|


---- 

### Converting Webots image into a BMP file (Dec 19, 2020)

Image processing is an important part of the Webots simulation world.  During the RoboCup Demonstration Rescue Competition, our team designed a Victim Detection Algorithm using OpenCV. In the past few months, Victor from our team has worked on image processing using C. He has been working on algorithms such as grayscale, binary, histogram, edge, and contour tracing. By making our own algorithms, we do not have to use the OpenCV library, which gives us the ability to embed image processing into different boards.

Victor tested his image processing algorithms on a Webots world since this could potentially provide an advantage over other teams, as the image processing could be faster and more reliable. In addition, by seeing the Webots image, we could then use it to test different algorithms or visualize ideas differently. 

Victor wrote the Webots image into a file, and then read the BGR channels into the bmp image. 

One of the challenges was in getting a BMP file format. This problem by solved with reading a BMP image first, and then overwriting the data. By getting an image of the same bitsize, height, and width, he was able to simply write the data onto the image without writing every byte.

The end result was an identical new image that could be used as another method for Webots testing or algorithm making.

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/bmpFileConvert.png?raw=true)|
| :--: |
| <b>Result of the new BMP file after conversion<b>|

----

### Contour Tracing Algorithm through C and BMP files (Dec 5, 2020)

During RoboCup Rescue Line and Maze, our team had done Computer Vision contour tracing using OpenCV’s findContours function. In the past month, Victor has focused on writing image processing code in C to make contour tracing algorithm capable of being used on embedded systems. By doing this, our team can use a vision system without a Raspberry Pi, nor the OpenCV library.

To begin, Victor used basic BMP image processing ideas to read the image in BMP format, convert it to a grayscale image, and convert it into a binary image. This resulted in an image with only two values, black and white.

Victor researched different contour tracing algorithms. The most basic algorithm was the Square Tracing Algorithm, which involves finding a 4-pixel community around the origin pixel.  Starting from the top left, and working left and down, he looked at each pixel to determine it’s value. If the value was black, then he would label this pixel as his “start pixel”, and begin the algorithm. He would check the pixel to the left of the start pixel, and if it was black, then he would label this as the “current pixel”. If the pixel was white, then he would go to the next pixel on the right. This algorithm would continue until he reached the “start pixel”. At the start pixel, this loop ended, and we had essentially found the edge of an the pixel.

However, another challenge was presented through holes. Holes are the pixels inside of the object that we have already found contours in. This problem was solved through using a hole-finding algorithm that checked for the min and max of each pixel, and shaded it out to white. The result was only contours that he wanted to see.  

This process is seen on the pictures below

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/Combined-Contour-Tracing-Image.png?raw=true)|
| :--: |
| <b>Result of the contour tracing being done</b>|



----
### Basic BMP Image Processing (Nov 28, 2020)

This past month, Victor has worked on basic image processing techniques using the C programming language. This is because our team wanted to see if we could potentially implement image processing ideas into an embedded system without needing OpenCV or Raspberry Pi. Our team also wanted to see if we could improve on our image processing solution during our win at RoboCup Simulation Demonstration Competition. The main file format that he used was the BMP file format because of its easy to use format, along with the ease of manipulation. 

Here are just a few of the projects that Victor worked on:


**Copying an image/reading a BMP image:**

This project involved simply reading an image, and then writing the image back into another file using the same BMP format.

**Grayscale transformation:**

There are two methods to do this, a weighted method where each R, G, and B value is weighted to a certain proportion, and the third method, which involves adding the R, G, B values and dividing by 3. The grayscale transformations that Victor did enables gives our team the ability to view specific colours more than others. 

**Binary Conversion:**

Binary conversion involves reading each pixel, and determining if the pixel is above or below a threshold. Most commonly, this threshold is set at 127 since it is right in the middle between 0 and 255. The end result is a purely black or white image. 

**Contrast Enhancement:**

There are two ways to do contrast enhancement, through histogram equalization, and through adding each pixel by a set value. The former method would be called contrast enhancement, while the latter one could be called brightening/darken. The histogram equalization method is the most interesting, as it results in an image with better focus and contrast. 

**Sharpening/Blurring/Edge Detection:**

Sharpening, Blurring, and Edge Detection in an image takes into affect the image’s community. This community is determined through a pixel’s kernel, which can be used to compare values around one pixel. 

|![](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/robotics/differences_in_sharpening.JPG?raw=true)|
| :--: |
| <b>Differences in the sharpness of images</b>|

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

## The following are videos that I made while on the team

### Communicating with other robots during the RCJ competition

{{< youtube hjoweaMZ8rc >}}

### Discussing our strategies for ball handling at the RCJ competition

{{< youtube IGBbXjDli18 >}}
