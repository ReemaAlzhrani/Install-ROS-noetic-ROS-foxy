# Install-ROS-noetic-ROS-foxy
## ROS or Robot Operating System :
ROS is an open-source framework for developing robot software.<br> It provides tools and libraries to help developers create complex robotics applications.<br>

## VIRTUAL MACHINE :
Intially , I used virtualBox but encoutered network connection issues happend between the virtual machine and my laptop , by switching to VMware workstation resolved these problems .
![ubuntu 20 04](https://github.com/user-attachments/assets/75a98d5b-72fc-4c2f-bc88-07a6b8844051)

### UBUNTU 20.04
After installing VMware I installed Ubuntu 20.04 64-bit then started to install ROS NOETIC <br>
## INSTALL ROS NOETIC : <br>
1- SETUP YOUR SOURCES.LIST <br>
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'<br>

2- SETUP YOUR KEYS  <br>
- sudo apt install curl<br>
- curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
![1 ROS NOETIC](https://github.com/user-attachments/assets/8d0a0bb4-3c46-4a0e-b899-a995f5bda29e) <BR>
3- INSTALLATION : <br>
-sudo apt update<br> 
(DESKTOP-FULL INSTALL) - sudo apt install ros-noetic-desktop-full<br>
![2ROS NOETIC](https://github.com/user-attachments/assets/504a4c10-d85c-40f2-93d0-fcfc7992ffe8)

4-ENVIRONMENT SETUP <br>
- source /opt/ros/noetic/setup.bash<br>
-echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc<br>
source ~/.bashrc<br>

5- DEPENDENCIES FOR BUILDING PACKAGES :<BR>
-sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential<BR>
 1- INITIALIZATION ROSDEP :<BR>
 -sudo apt install python3-rosdep<BR>
-sudo rosdep init<BR>
-rosdep update<BR>
![3ROS NOETIC](https://github.com/user-attachments/assets/03b87cf1-aaab-4e23-b7df-38a5d93a0787)

<BR>
than we can start the ROS (master node ) = roscore 
<br>
------------------------------------------------------------------ <br>
 <br># INSTALL ROS FOXY :

1- SET LOCALE :
-locale  <br>
-sudo apt update && sudo apt install locales <br>
-sudo locale-gen en_US en_US.UTF-8 <br>
-sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8 <br>
-export LANG=en_US.UTF-8 <br>
-locale  -> TO VERTIFY  <br>
![1-ROS2 FOXY](https://github.com/user-attachments/assets/eb14437d-a1e9-4bf4-a199-0ad0611d26ee)


2- SETUP SOURCES ;
- sudo apt install software-properties-common <br>
- sudo add-apt-repository universe <br>
- sudo apt update && sudo apt install curl -y <br>
- sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg <br>
-echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(. /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null

![2-ROS2 FOXY](https://github.com/user-attachments/assets/8227ddb3-d356-4e9e-aa68-ebcb8b2e2d6b)

3- INSTALL ROS2 PACKAGES :
-sudo apt update <br>
-sudo apt update <br>
-sudo apt install ros-foxy-desktop python3-argcomplete <br>
![4ROS2 FOXY](https://github.com/user-attachments/assets/f784cac7-5ae4-4959-a743-f3efed4da70e)


4- ENVIRONMENT SETUP 
-source /opt/ros/foxy/setup.bash <br>


Then we can try some examples like talker <br>
source /opt/ros/foxy/setup.bash
ros2 run demo_nodes_cpp talker








 
