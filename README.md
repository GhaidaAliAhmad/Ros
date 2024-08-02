# Ros

### Part 1: Installing ROS Noetic on Ubuntu 20.04

1. **Set up your sources.list**
   ```bash
   sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
   ```

2. **Set up your keys**
   ```bash
   sudo apt install curl # if you haven't already installed curl
   curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
   ```

3. **Update your package index**
   ```bash
   sudo apt update
   ```

4. **Install ROS Noetic**
   ```bash
   sudo apt install ros-noetic-desktop-full
   ```

5. **Initialize rosdep**
   ```bash
   sudo rosdep init
   rosdep update
   ```

6. **Environment setup**
   Add the following line to your `.bashrc` file:
   ```bash
   echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
   source ~/.bashrc
   ```

7. **Install dependencies for building packages**
   ```bash
   sudo apt install python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
   ```

### Part 2: Installing ROS 2 Foxy on Ubuntu 20.04

1. **Set up your sources.list**
   ```bash
   sudo apt update && sudo apt install curl gnupg2 lsb-release
   sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
   sudo sh -c 'echo "deb [arch=amd64] http://packages.ros.org/ros2/ubuntu $(lsb_release -cs) main" > /etc/apt/sources.list.d/ros2-latest.list'
   ```

2. **Update your package index**
   ```bash
   sudo apt update
   ```

3. **Install ROS 2 Foxy**
   ```bash
   sudo apt install ros-foxy-desktop
   ```

4. **Environment setup**
   Add the following line to your `.bashrc` file:
   ```bash
   echo "source /opt/ros/foxy/setup.bash" >> ~/.bashrc
   source ~/.bashrc
   ```
