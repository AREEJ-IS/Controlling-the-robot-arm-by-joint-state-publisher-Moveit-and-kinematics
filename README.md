# Controlling-the-robot-arm-by-joint-state-publisher-Moveit-and-kinematics

## step1: Create a ROS Workspace (Catkin)

````
mkdir catkin_ws
````
then you can go inside your new folder:
````
cd catkin_ws
````
then we are going to create a source (make sure it it exactly src inside thr catkin work space)
````
mkdir src
````
<img width="381" alt="ف" src="https://github.com/user-attachments/assets/ee365c31-6ae2-4c35-9bb5-47810bbe0649">

now make sure that you are inside the catkin_ws folder (not inside the src folder) then we can start to compile by running the command :
````
catkin_make
````
<img width="960" alt="ا" src="https://github.com/user-attachments/assets/f18a7dc2-6112-46e5-8a64-5cc1b66c4345">


basicaally this is gonna compile everything in the workspace, install stuff, etc...



now if we run the command ```ls``` we see that we have two new folders (build and devel)

if you go to the devel folder : ```cd devel/``` then ```ls```


<img width="667" alt="س copy" src="https://github.com/user-attachments/assets/13d3df03-867a-4d8c-b1b8-4b80ff2f65fe">


here we see something called (setup.bash) we will need to source this (setup.bash) script if we want to be able to use the code that we have written in our catkin workspace.

so, to source this we will need to:

````
source ~/catkin_ws/devel/setup.bash

````
once you have run this command you can use your custom ROS code

last thing here is to run  ```gedit ~/.bashrc``` then this window will appears

<img width="385" alt="غ" src="https://github.com/user-attachments/assets/2563aa96-8bdf-43d8-a8cf-6094e2ec5ca6">


at the end or the window we have the source line for our global ROS installation . so we will add this line ```source ~/catkin_ws/devel/setup.bash``` (after) the global ROS installation

<img width="383" alt="س copy 3" src="https://github.com/user-attachments/assets/a42ed7be-aca9-415f-a9c5-cca6c802dd48">

now save and quit the file. you should have those two lines so you can see your global ros installation as kind of a first level, and then your custom workspace here have the second level. you need to source both the global ROS installation and your catkin workspace, so you can use your code with ROS functionalities.






## Installing the package arduino_robot_arm

## Controlling the motors

## showing the graph

## Gazebo

## MoveIt controlling

