# CarND-Extended-Kalman-Filter-Project
Self-Driving Car Engineer Nanodegree Program - Extended Kalman Filter Implementation

This project consists of implementing an Extended Kalman Filter (EKF) with C ++. The objective is to track the position and speed of a bicycle using noisy Radar and Lidar measurements, which are generated in a simulator provided by Udacity ([link](https://github.com/udacity/self-driving-car-sim/releases)). The EKF filter fuses these measurements to predict the position and velocity of the bicycle.

---

## 0. Rubric Points

This project consider the following rubric points ([link][https://review.udacity.com/#!/rubrics/1962/view]).


## Compiling

The code should compile without errors. I did not modify the CMakeLists.txt provided by Udacity. The following steps show how to compile this project:

1. Clone this repo.
2. Make a build directory: `mkdir build && cd build`
3. Compile: `cmake .. && make` 
   * On windows, you may need to run: `cmake .. -G "Unix Makefiles" && make`
4. Run it: `./ExtendedKF `

## Runnig the EKF Filter - Accuracy

The following figure shows an image of the output visualized in the simulator for the dataset 1. The green triangles correspond to the filter estimation, the red circles are the lidar measurements, and the blue circles are the radar measurements.

In this project it is required to have a Root Mean Squared errors maximum of: [px = .11, py = .11,  vx = 0.52,  vy = 0.52] . Analyzing the results shown in the image, it is observed that my implementation meets this requirement, having an RMSE of 5. In addition to this, the image shows a well-defined trajectory of the position estimated.

## Follows the Correct Algorithm.

TThe EKF implementation can be found in [src/kalman_filter.cpp](https://github.com/JKWalleiee/CarND-Extended-Kalman-Filter-Project/blob/master/src/kalman_filter.cpp). The processing flow can be found in [src/FusionEKF.cpp]](https://github.com/JKWalleiee/CarND-Extended-Kalman-Filter-Project/blob/master/src/FusionEKF.cpp) (Update step in line 149 and Predict step in lines 162-172).

## Code Efficiency
An example of this calculation optimization is when the Q matrix is calculated ([src/FusionEKF.cpp](https://github.com/JKWalleiee/CarND-Extended-Kalman-Filter-Project/blob/master/src/FusionEKF.cpp) lines 138-146.)


## OPTIONAL

### Dataset 2
The following figure shows an image of the output visualized in the simulator for the dataset 1. The final RSME meet the required limits (<= [.11, .11, 0.52, 0.52] ).



