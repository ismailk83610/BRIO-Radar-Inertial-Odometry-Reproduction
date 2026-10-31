# BRIO Odometry Reproduction

## Project Overview

This project aims to reproduce the research paper:

**"A Robust Baro-Radar-Inertial Odometry M-Estimator for Multicopter Navigation in Cities and Forests"**

The main objective is to estimate a drone's position, velocity, and orientation by combining measurements from multiple sensors without relying on GPS.

### Sensors Used

The system uses three sensors:

1. **IMU (Inertial Measurement Unit)** – Measures acceleration and angular velocity.
2. **Radar** – Measures radial velocities and directions of detected objects.
3. **Barometer** – Measures atmospheric pressure to help estimate altitude.

Additionally, **Zero-Velocity Tracking** is used to improve state estimation when the drone is stationary.

## How the System Works

The overall process is:

1. Collect sensor measurements from IMU, Radar, and Barometer.
2. Synchronize measurements from different sensors.
3. Create factors based on the sensor measurements.
4. Connect factors and drone states using a factor graph.
5. Calculate residual errors between predicted and measured values.
6. Apply robust loss functions to reduce the influence of incorrect measurements.
7. Optimize the factor graph to estimate the drone's state.
8. Obtain the estimated position, velocity, and orientation.

## Methods

The project focuses on:

- IMU preintegration
- Radar Doppler factors
- Barometer factors
- Zero-velocity tracking factors
- Factor graph optimization
- Robust loss functions (Welsch and Fair)
- State estimation using GTSAM

## Project Implementation

The project will be developed in the following stages:

**Phase 1: Understanding State Estimation**

Study the drone state, including position, velocity, orientation, and IMU biases.

**Phase 2: Understanding Sensors**

Study the IMU, radar, barometer, coordinate frames, and sensor measurements.

**Phase 3: Understanding Sensor Factors**

Study IMU preintegration, radar Doppler residuals, barometer residuals, and zero-velocity tracking.

**Phase 4: Understanding Optimization**

Study factor graphs, residual errors, covariance matrices, robust loss functions, and optimization.

**Phase 5: Implementation**

Set up the development environment, examine the original code and datasets, and reproduce the estimation pipeline.

**Phase 6: Evaluation**

Evaluate the estimated trajectories and compare the results with those reported in the research paper.

## Expected Output

The expected outputs are:

- Estimated drone trajectory
- Estimated position (x, y, z)
- Estimated velocity
- Estimated orientation
- Visualization of the estimated trajectory
- Evaluation of estimation errors
- Comparison with the original paper's results

## Reference

**Research Paper:**  
Girod et al., *A Robust Baro-Radar-Inertial Odometry M-Estimator for Multicopter Navigation in Cities and Forests*, 2024.

**Original Implementation:**  
https://github.com/ethz-asl/rio

**Paper:**  
https://arxiv.org/abs/2408.05764

## Project Status

🚧 Work in Progress

Currently studying the theoretical concepts and preparing for implementation.
