# ros-install
First step :

download VirtualBox that you use it to install other OS in your device.

The next stage is installing Ubuntu, and these are the instructions :

1-Download ubuntu https://releases.ubuntu.com/20.04/

2- Open VirtualBox then click new + .

3- VirtualBox is intelligent enough to automatically set the type and version to Linux and Ubuntu(64bit) when you name it, then click next..

4-select the amount of memory size you want .

5-in Hard drive select your preferred option, click "create".

6-In Hard disk file type don't change it (VDI default) then click next.

7-choose preferd stordge size .

8-In file location and size choose what you like but ((make sure to have enough space)), then click create..

9-Right-click the OS you just created, then select settings, select Advance, create a Shared Clipboard, and select Drag/Drop to Bidirectional. so that you can copy and paste between your real OS and the virtual OS. Then go to the system and processor, marking the end of the green is preferable.

10-Go to storage next, where you will link the privately downloaded version of Ubuntu with the VOS you established by clicking the empty word, then clicking the blue circle, choosing disk file, selecting the downloaded Ubuntu version, and then clicking OK. And you've finished configuring it in VirtualBox.
11-Click start , install ubuntu then choose your keyboard language then click continue.

12- make sure to click on Install third-paty .

13-install .

14-set your location then click continue.

15-set your Name and Password , continue.

16- finally restart VOS.

now for installing ROS ... 

follow the guide in https://wiki.ros.org/noetic/Installation/Ubuntu to install ROS .



How to install ROS Melodic on Jetson Nano

((make sure the internet connection works fine))

1- Open Terminal and copy paste this command: (sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list') 

2- Update package list: (sudo apt update)

3- Then this command : (sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654)..
after this put (y) to begin

4-put this command :(sudo apt-get update) then this :(sudo apt install ros-melodic-desktop-full) .
then again put (y) to accept and press Enter to complete the installation...

5-to Set up the environment variables type this command : (echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc) then (source ~/.bashrc).

6-Install some other tools that you will work with in ROS. After you type the command below, type Y and Enter to complete the download process: (sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential) then type Y .

7-Then start rosdep. Before using ROS, you must install this (sudo apt install python-rosdep > (sudo rosdep init) >). (rosdep update) , Check the ROS version that you have set up. If your ROS version appears in the report, then your installation of ROS was successful. Roversion -d
