# FCND - Building an Estimator

## Writeup / README

### 1. Provide a Writeup / README that includes all the rubric points and how you addressed each one.  You can submit your writeup as markdown or pdf

You're reading it! Below I describe how I addressed each rubric point and where in my code each point is handled.

### Implement Estimator

#### 1. Determine the standard deviation of the measurement noise of both GPS X data and Accelerometer X data.

##### The calculated standard deviation should correctly capture ~68% of the sensor measurements. Your writeup should describe the method used for determining the standard deviation given the simulated sensor measurements.

As seen below is the implementation of the body rate control.

![Code Image](./misc/code/body_rate_control.PNG)

#### 2. Implement a better rate gyro attitude integration scheme in the `UpdateFromIMU()` function.

##### The improved integration scheme should result in an attitude estimator of < 0.1 rad for each of the Euler angles for a duration of at least 3 seconds during the simulation. The integration scheme should use quaternions to improve performance over the current simple integration scheme.

As seen below is the implementation of the roll pitch.

![Code Image](./misc/code/roll_pitch_control.PNG)

#### 3. Implement all of the elements of the prediction step for the estimator.

##### The prediction step should include the state update element (PredictState() function), a correct calculation of the Rgb prime matrix, and a proper update of the state covariance. The acceleration should be accounted for as a command in the calculation of gPrime. The covariance update should follow the classic EKF update equation.

As seen below is the implementation of the altitude controller.

![Code Image](./misc/code/altitude_control.PNG)

#### 4. Implement the magnetometer update.

##### The update should properly include the magnetometer data into the state. Note that the solution should make sure to correctly measure the angle error between the current state and the magnetometer value (error should be the short way around, not the long way).

As seen below is the implementation of the lateral position control.

![Code Image](./misc/code/lateral_position_control.PNG)

#### 5. Implement the GPS update.

##### The estimator should correctly incorporate the GPS information to update the current state estimate.

As seen below is the implementation of the Yaw control.

![Code Image](./misc/code/yaw_control.PNG)

### Flight Evaluation

#### 1. Meet the performance criteria of each step.

##### For each step of the project, the final estimator should be able to successfully meet the performance criteria with the controller provided. The estimator's parameters should be properly adjusted to satisfy each of the performance criteria elements.

Here is the result of the scenarios

#### 2. De-tune your controller to successfully fly the final desired box trajectory with your estimator and realistic sensors.

##### The controller developed in the previous project should be de-tuned to successfully meet the performance criteria of the final scenario (<1m error for entire box flight).

Here is the result of the scenarios