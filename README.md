
# Kinematic computation 

## Overview

This notebook demonstrates a regression-based approach to modeling robotic motion using machine learning. It focuses on learning the **forward kinematics** of a simple 2-DOF robotic arm from data.

Instead of relying purely on analytical equations, the notebook trains a model to approximate the mapping:

```
(theta1, theta2) → (x, y)
```

---



The notebook walks through the full pipeline:

### 1. Data Generation

* Simulates joint angles in the range `[-π, π]`
* Computes end-effector position using forward kinematics
* Adds small noise to mimic real-world sensor data

### 2. Exploratory Analysis

* Visualizes the robot workspace
* Examines feature distributions
* Checks correlations

### 3. Model Training

* Uses a neural network (`MLPRegressor`)
* Applies feature scaling
* Trains on simulated data

### 4. Evaluation

* Measures performance using Mean Squared Error (MSE)
* Compares predictions with ground truth

### 5. Model Export

* Saves the trained model using `joblib`

### 6. Testing

* Loads the exported model
* Runs predictions on new joint configurations

---


