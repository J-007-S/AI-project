# IMU Data Denoising: A Learning Journey

## Paper Reference
-## Denoising IMU Gyroscope with Deep Learning for Open-Loop Attitude Estimation
-## Overview [[IEEE paper](https://ieeexplore.ieee.org/document/9119813), [preprint paper]

## Project Overview
This repository documents my journey in replicating and understanding the method presented in the paper for denoising IMU data using RNN. It's a personal learning project where I explore, experiment, and gradually build up the implementation.

## Reference Resources
- **GitHub Repository**: [BahMoh/denoise-imu-gyro](https://github.com/BahMoh/denoise-imu-gyro)
- **Recommended Up主**:
  - 跟李沐学AI
  - 我是土堆
  - 
## Dataset Exploration
I've been looking into several datasets that could be useful for this project:

### EuRoC MAV Dataset
- **Source**: [EuRoC MAV Dataset](https://projects.asl.ethz.ch/datasets/doku.php?id=kmavvisualinertialdatasets)
- **Description**: This dataset contains visual-inertial data collected on-board a Micro Aerial Vehicle (MAV). It includes stereo images, synchronized IMU measurements, and accurate motion and structure ground-truth.

### TUM Visual-Inertial Dataset
- **Source**: [TUM Visual-Inertial Dataset](https://paperswithcode.com/dataset/tum-visual-inertial-dataset)
- **Description**: A diverse set of sequences in different scenes for evaluating visual-inertial odometry. It provides camera images with high resolution and dynamic range.

### OpenVINS Platform
- **Source**: [OpenVINS](https://docs.openvins.com/)
- **GitHub**: [rpng/open_vins](https://github.com/rpng/open_vins)
- **Description**: An open-source platform for visual-inertial navigation research. It includes a state-of-the-art filter-based visual-inertial estimator.

## Data Processing Insights
### Noise Simulation
I've been working on simulating real-world conditions by adding noise to the IMU data. The `add_noise` method generates Gaussian noise with different intensities for various sensor axes, mimicking the errors that actual sensors might introduce.

## Understanding the Data
### Synchronization
IMU data and ground-truth data are synchronized using timestamps. This ensures that each IMU reading corresponds accurately to the position and orientation data.

### Interpolation Method
The Slerp (Spherical Linear Interpolation) method is used for smooth rotation transitions. This is crucial for applications like robot path planning or animation generation where smooth motion is required.

## Network Architecture Exploration
### BaseNet
I've implemented a general convolutional neural network structure called BaseNet. It consists of multiple convolutional layers, batch normalization, and GELU activation functions. The use of dilated convolutions helps expand the receptive field, allowing the network to capture longer-term dependencies in the data.

### GyroNet Extension
Building upon BaseNet, I've developed GyroNet specifically for processing gyroscope data. It incorporates rotation matrix transformations and standard deviation predictions to refine the network outputs, making it suitable for tasks requiring high-precision orientation estimation.
