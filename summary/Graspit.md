# A detailed environment configuration for Mano hand object grasp generation

% Ubuntu 18.04

% install graspit

sudo apt-get update

sudo apt-get upgrade

sudo apt-get install libqt4-dev

sudo apt-get install libqt4-opengl-dev

sudo apt-get install libqt4-sql-psql

sudo apt-get install libcoin80-dev

sudo apt-get install libsoqt4-dev

sudo apt-get install libblas-dev

sudo apt-get install liblapack-dev

sudo apt-get install libqhull-dev

sudo apt-get install libeigen3-dev

sudo apt-get install libcanberra-gtk-module libcanberra-gtk3-module 

sudo apt-get install git

sudo apt-get install cmake

git clone https://github.com/graspit-simulator/graspit.git

cd graspit

mkdir build

cd build

cmake ..

make -j5

sudo make install

% set env

sudo gedit /etc/environment

%export GRASPIT=/home/your_user_name/.graspit

export   GRASPIT=/home/parallels/.graspit    % if use GRASPIT=~/.graspit, graspit_commander will fail becasue can not open file in ~/.graspit

gedit ~/.bashrc

export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/lib

source ~/.bashrc

source /etc/environment

printenv GRASPIT

graspit_simulator 

% install ros  http://wiki.ros.org/melodic/Installation/Ubuntu

sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

sudo apt update

sudo apt install ros-melodic-ros-base 

echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc

source ~/.bashrc

% install ros interface and commandline

% install in the folder graspit

(cd ~/graspit)

mkdir -p graspit_ros_ws/src

cd graspit_ros_ws/src

catkin_init_workspace . 

git clone https://github.com/graspit-simulator/graspit_interface.git

git clone https://github.com/graspit-simulator/graspit_commander.git

cd graspit_ros_ws

catkin_make

source devel/setup.bash

roslaunch graspit_interface graspit_interface.launch

%test for graspit_commander

sudo apt install python-pytest % for test

%In one terminal:

source devel/setup.bash

roslaunch graspit_interface graspit_interface.launch

%Then in a second terminal:

source devel/setup.bash

roscd graspit_commander

py.test % success after all passed

% install mano grasp

% install in the folder grasp

sudo gedit /etc/environment 

% GRASPIT_PLUGIN_DIR is the position of libgraspit_interface.so

export GRASPIT_PLUGIN_DIR=/home/parallels/graspit/graspit_ros_ws/devel/lib

(cd ~/graspit)

git clone https://github.com/ikalevatykh/mano_grasp.git

cd mano_grasp

python setup.py install --user --graspit_dir=$GRASPIT

pip install numpy

pip install pyyaml

pip install transforms3d

pip install joblib

sudo apt install xvfb

pip install yapf

pip install futures

% Note that the code in graspit_process.py

% the function of subprocess.Popen will not report an error even we do not have a correct environment configuration

% especially, the address of GRASPIT_PLUGIN_DIR

%In one terminal:

roscore

%Then in a second terminal:

(cd ~/graspit/graspit_ros_ws)

source devel/setup.bash

roscd graspit_commander

python -m mano_grasp.generate_grasps --path_out /home/parallels/Desktop/out
