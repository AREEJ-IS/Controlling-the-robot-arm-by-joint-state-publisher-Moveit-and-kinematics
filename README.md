<img width="960" alt="2" src="https://github.com/user-attachments/assets/804d33f5-4eea-475f-b1fc-54917efec9b1"># Controlling-the-robot-arm-by-joint-state-publisher-Moveit-and-kinematics

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

<img width="981" alt="1" src="https://github.com/user-attachments/assets/bf0abd77-b2f0-4345-bb5b-634dbda8163c">

now make sure that you are inside the catkin_ws folder (not inside the src folder) then we can start to compile by running the command :
````
catkin_make
````

<img width="960" alt="2" src="https://github.com/user-attachments/assets/c4fe4e87-f14d-4c49-9adc-c3e977ad5953">


basicaally this is gonna compile everything in the workspace, install stuff, etc...



now if we run the command ```ls``` we see that we have two new folders (build and devel)

if you go to the devel folder : ```cd devel/``` then ```ls```

<img width="954" alt="3" src="https://github.com/user-attachments/assets/2f166ac9-29e0-4095-bde2-e921698f6aa8">


here we see something called (setup.bash) we will need to source this (setup.bash) script if we want to be able to use the code that we have written in our catkin workspace.

so, to source this we will need to:

````
source ~/catkin_ws/devel/setup.bash

````
once you have run this command you can use your custom ROS code

last thing here is to run  ```gedit ~/.bashrc``` then this window will appears

<img width="985" alt="4" src="https://github.com/user-attachments/assets/84d5c9ea-a2b4-47d8-8a81-4eb146ea8e2b">



at the end or the window we have the source line for our global ROS installation . so we will add this line ```source ~/catkin_ws/devel/setup.bash``` (after) the global ROS installation

<img width="983" alt="5" src="https://github.com/user-attachments/assets/72e43ada-c7c0-47dc-a2de-bc675bad172d">

now save and quit the file. you should have those two lines so you can see your global ros installation as kind of a first level, and then your custom workspace here have the second level. you need to source both the global ROS installation and your catkin workspace, so you can use your code with ROS functionalities.


## Installing the package arduino_robot_arm
1- Add the “arduino_robot_arm” package to “src” folder cd src then copy this command :
````
sudo apt install git
````
<img width="970" alt="6" src="https://github.com/user-attachments/assets/9e54e3f1-5ae5-4f24-a51e-3d02642268a9">

2- ```git clone https://github.com/smart-methods/arduino_robot_arm````

<img width="911" alt="7" src="https://github.com/user-attachments/assets/8957dd6a-dbb3-41b5-b78c-b172700d4cbe">

3- now go back to the (catkin_ws) using command ```` cd ..```` ,then
````
rosdep install --from-paths src --ignore-src -r -y
````
<img width="953" alt="8" src="https://github.com/user-attachments/assets/d3ae7b91-7275-4cba-83b8-204b86d4c1dd">


4- run the command```` sudo apt-get install ros-noetic-moveit````
<img width="960" alt="9" src="https://github.com/user-attachments/assets/3b76d3b4-1aa4-4fdc-a72a-4fe2d0eacbe8">

5- run the command
````
sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
````
<img width="900" alt="10" src="https://github.com/user-attachments/assets/1db0ccbb-68d8-4739-83ab-95b1a6388d56">

6-````sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher````
<img width="927" alt="11" src="https://github.com/user-attachments/assets/613694d5-1c89-4fbb-a6d6-40dd23503683">

7-````sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control````
<img width="927" alt="12" src="https://github.com/user-attachments/assets/ad20ec19-52e6-410a-901c-c333b26d8a55">

8- compile the package
````
catkin_make
````

## Controlling the motors
* when you run this command the widows will apears
````
roslaunch robot_arm_pkg check_motors.launch
````
<img width="925" alt="88 copy" src="https://github.com/user-attachments/assets/dcc943bd-ea5f-4afd-a95a-7c4a0f0e4e41">

You can move it as you wish too!
<img width="927" alt="cc copy" src="https://github.com/user-attachments/assets/e8584bfe-230f-4d34-9c3b-550ae6105ca0">

## showing the graph
if you want to see a graph of what is happening at this time just run this command
````
rqt_graph
````
<img width="901" alt="555 copy" src="https://github.com/user-attachments/assets/f53a9ad9-6244-4963-bda7-664084a4b9e0">

## Gazebo
run the command :
````
roslaunch robot_arm_pkg check_motors_gazebo.launch
````
<img width="919" alt="gz" src="https://github.com/user-attachments/assets/76863838-1844-4ef3-a26d-03a69f202a99">

## MoveIt controlling
````
roslaunch moveit_pkg demo.launch
````
<img width="924" alt="5;00 copy" src="https://github.com/user-attachments/assets/4db86d16-a980-43c4-a5c3-f3d3fc71f037">

