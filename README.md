# Unscented_Kalman_FilterUnscented_Kalman_Filter
Sensor Fusion UKF Highway Project Starter Code



In this project you will implement an Unscented Kalman Filter to estimate the state of multiple cars on a highway using noisy lidar and radar measurements. Passing the project requires obtaining RMSE values that are lower that the tolerance outlined in the project rubric.

The main program can be built and ran by doing the following from the project top directory.

mkdir build
cd build
cmake ..
make
./ukf_highway
Note that the programs that need to be written to accomplish the project are src/ukf.cpp, and src/ukf.h

The program main.cpp has already been filled out, but feel free to modify it.



main.cpp is using highway.h to create a straight 3 lane highway environment with 3 traffic cars and the main ego car at the center. The viewer scene is centered around the ego car and the coordinate system is relative to the ego car as well. The ego car is green while the other traffic cars are blue. The traffic cars will be accelerating and altering their steering to change lanes. Each of the traffic car's has it's own UKF object generated for it, and will update each indidual one during every time step.

The red spheres above cars represent the (x,y) lidar detection and the purple lines show the radar measurements with the velocity magnitude along the detected angle. The Z axis is not taken into account for tracking, so you are only tracking along the X/Y axis.

Other Important Dependencies
cmake >= 3.5
All OSes: click here for installation instructions
make >= 4.1 (Linux, Mac), 3.81 (Windows)
Linux: make is installed by default on most Linux distros
Mac: install Xcode command line tools to get make
Windows: Click here for installation instructions
gcc/g++ >= 5.4
Linux: gcc / g++ is installed by default on most Linux distros
Mac: same deal as make - install Xcode command line tools
Windows: recommend using MinGW
PCL 1.2
Basic Build Instructions
Clone this repo.
Make a build directory: mkdir build && cd build
Compile: cmake .. && make
Run it: ./ukf_highway
Editor Settings
We've purposefully kept editor configuration files out of this repo in order to keep it as simple and environment agnostic as possible. However, we recommend using the following settings:

indent using spaces
set tab width to 2 spaces (keeps the matrices in source code aligned)
Code Style
Please stick to Google's C++ style guide as much as possible.

Generating Additional Data
This is optional!

If you'd like to generate your own radar and lidar modify the code in highway.h to alter the cars. Also check out tools.cpp to change how measurements are taken, for instance lidar markers could be the (x,y) center of bounding boxes by scanning the PCD environment and performing clustering. This is similar to what was done in Sensor Fusion Lidar Obstacle Detection.

Project Instructions and Rubric
This information is only accessible by people who are already enrolled in Sensor Fusion. If you are enrolled, see the project page in the classroom for instructions and the project rubric.
