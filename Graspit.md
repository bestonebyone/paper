install Ubuntu 18.04

sh Anaconda3-2019.10-Linux-x86_64.sh (no sudo here)

conda create --name graspit python=3.7
conda activate graspit

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
conda install git
conda install cmake

git clone https://github.com/graspit-simulator/graspit.git
cd graspit
%export GRASPIT=$PWD
mkdir build
cd build
cmake ..
make -j5
sudo make install

sudo gedit /etc/environment
GRASPIT=~/.graspit

gedit ～/.bashrc
%export GRASPIT=/home/your_user_name/graspit
LD_LIBRARY_PATH=/usr/local/lib:$LD_LIBRARY_PATH

source ~/.bashrc
source /etc/environment
printenv GRASPIT

graspit_simulator 

sudo apt install ros-melodic-ros-base
%sudo apt-get install ros-indigo-ros-base

echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
source ~/.bashrc

mkdir -p graspit_ros_ws/src
cd graspit_ros_ws/src
catkin_init_workspace . 
git clone https://github.com/graspit-simulator/graspit_interface.git
git clone https://github.com/graspit-simulator/graspit_commander.git
cd graspit_ros_ws
catkin_make


source devel/setup.bash
roslaunch graspit_interface graspit_interface.launch