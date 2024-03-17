## ROS Publisher Subscriber with VS Code

The settings for using the ROS code are added in the `.vscode` folder. To add more features, please update the files in the `.vscode` folder.

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
For further details, visit [ROS Official Website](http://wiki.ros.org/ROS/Installation)

### Dependencies
- ROS
- C++

### Build
```
mkdir ros_packages && cd ros_packages
mkdir pub_sub && cd pub_sub
mkdir catkin_ws && cd catkin_ws
git clone git@github.com:arghadeep25/ROS-Pub-Sub-VSCode.git
mv ROS-Pub-Sub-VSCode/* . && rm -rf ROS-Pub-Sub-VSCode/
catkin_make
```

### Usage
Run the following commands in different terminals separately
- `roscore`
- `rosrun pub_sub_test pub`
- `rosrun pub_sub_test sub`