## ROS Publisher Subscriber with VS Code

### Install ROS
```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
sudo apt update
sudo apt install ros-noetic-desktop-full
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
sudo apt install python3-rosdep
sudo rosdep init
rosdep update
```

### Dependencies
- ROS
- C++

### Usage
```
mkdir ros_packages && cd ros_packages
mkdir catkin_ws && cd catkin_ws
git clone git@github.com:arghadeep25/ROS-Pub-Sub-VSCode.git
mv ROS-Pub-Sub-VSCode/* .
catkin_make
```