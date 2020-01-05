This is a simulation of Kuka youBot designed in Gazebo, also there are some programas to control the arm.
The main task is a "Pick and Place"

Installation
------------

### System requirements: 
* Linux 18.04 LTS
* ROS Melodic
* Gazebo (Installed with full version of ROS)


Create and initialize catkin workspace (i. e. miRobot):

    mkdir -p ~/miRobot/src
    cd ~/miRobot/src
    catkin_init_workspace
    cd ..
    catkin_make

Clone the youBot GUI sources to /src folder:
    
    cd ~/miRobot/src
    git clone https://github.com/CamiloEsc/miRobot.git

Compile the youbot GUI by typing:

    cd ~/miRobot
    catkin_make

Usage
------------

The youBot GUI give you  graphical user interface app to communicate with youBot arm via youbot_driver. You can move youBot arm with joints or in the global coordinate system, create list of points and create automatic program with PTP or LIN movements between these points. You can open and close youBot gripper in automatic or manual mode.

To run youbot_gui you need to follow this commands:

    cd ~/miRobot
    source devel/setup.bash
    roslaunch miRobot miRobot.launcher

To control the arm you have to built your own applications like "programas" 
The command tu pub over the Kuka youBot through the plugin is e.g: 


rostopic pub youbot std_msgs/String "e ../miRobot/src/miRobot/programas/pick" 


License
------------

This software is published under a dual-license: GNU Lesser General Public
License LGPL 2.1 and BSD license. The dual-license implies that users of this
code may choose which terms they prefer.

youBot's ROS packages were downloaded from official youBot repository.
Our GUI is based on qt_ros package's example.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU Lesser General Public License LGPL and the BSD license for more details.
