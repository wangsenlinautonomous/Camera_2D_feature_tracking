# 2D Feature Tracking (Camera Based)

## Dependencies for Running Locally
* cmake >= 2.8
  * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1 (Linux, Mac), 3.81 (Windows)
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* OpenCV >= 4.1
  * This must be compiled from source using the `-D OPENCV_ENABLE_NONFREE=ON` cmake flag for testing the SIFT and SURF detectors.
  * The OpenCV 4.1.0 source code can be found [here](https://github.com/opencv/opencv/tree/4.1.0)
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same deal as make - [install Xcode command line tools](https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)

## Basic Build Instructions

1. Clone this repo.
2. Make a build directory in the top level directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./2D_feature_tracking`.

## Results

TASK MP.7
Your seventh task is to count the number of keypoints on the preceding vehicle for all 10 images and take note of the distribution of their neighborhood size. Do this for all the detectors you have implemented.

![result](https://user-images.githubusercontent.com/40875720/68811131-db334a00-06aa-11ea-8353-3ab48b83f022.PNG)



TASK MP.8
Your eighth task is to count the number of matched keypoints for all 10 images using all possible combinations of detectors and descriptors. In the matching step, use the BF approach with the descriptor distance ratio set to 0.8.

![result2](https://user-images.githubusercontent.com/40875720/68811136-dec6d100-06aa-11ea-9b2a-e6e1f87b9dce.PNG)


TASK MP.9

![result3](https://user-images.githubusercontent.com/40875720/68811139-e1292b00-06aa-11ea-8181-f8cf56e1c146.PNG)


#### Neighborhood size

As far as distribution of neighborhood size of keypoints detected on preceding vehicle is concerned, some of the detector methods have fixed neighborhood sizes, namely:

* SHITOMASI -- 4
* HARRIS -- 6
* FAST -- 7


Based on these scores my recommendations are:


| rank | detector | descriptor |
|:------:|:------:|:------:|
| 1 | FAST | ORB |
| 2 | FAST | BRIEF |
| 3 | SHITOMASI | BRIEF |
