# cartographer

## [Building & Installing Cartographer](https://google-cartographer-ros.readthedocs.io/en/latest/compilation.html#)
* Ubuntu 16.04
* Python 2.7
```
$ sudo apt-get update
$ sudo apt-get install -y python-wstool python-rosdep ninja-build
```
If Anaconda is installed on your workstation, you'd better create a virtual environment with python 2.7.
```
$ mkdir ros_env
$ cd ros_env
$ virtualenv --python=python2.7 _venv_py2.7
$ source _venv_py2.7/bin/activate
(_venv_py2.7) $ mkdir catkin_ws
(_venv_py2.7) $ cd catkin_ws
(_venv_py2.7) $ wstool init src
(_venv_py2.7) $ wstool merge -t src https://raw.githubusercontent.com/googlecartographer/cartographer_ros/master/cartographer_ros.rosinstall
(_venv_py2.7) $ wstool update -t src
```
```
(_venv_py2.7) $ src/cartographer/scripts/install_proto3.sh
(_venv_py2.7) $ sudo rosdep init
(_venv_py2.7) $ rosdep update
(_venv_py2.7) $ export ROS_DISTRO=kinetic
(_venv_py2.7) $ rosdep install --from-paths src --ignore-src --rosdistro=${ROS_DISTRO} -y
```
If the step ```rosdep install``` stops due to error like 


https://google-cartographer-ros.readthedocs.io/en/latest/index.html

https://github.com/googlecartographer/cartographer

https://github.com/googlecartographer

source /opt/ros/kinetic/setup.bash

http://wiki.ros.org/kinetic/Installation/Ubuntu:

* sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
* sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116
* sudo apt-get update
