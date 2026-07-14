# Quadrotor Controller and Observer Design

A modern control engineering project focused on modeling, analyzing, and controlling a nonlinear quadrotor system using state-space methods, state feedback, LQR control, observer design, Kalman filtering, and digital control techniques.

## Project Overview

A quadrotor is a nonlinear and coupled dynamic system whose stable control requires accurate modeling, state estimation, and appropriate controller design.

In this project, the nonlinear dynamic model of the quadrotor is first developed. The system is then linearized around an equilibrium operating point to obtain a linear state-space representation.

The linearized model is analyzed in terms of stability, controllability, and observability. The validity range of the linear model is also investigated through simulation.

State-feedback and LQR controllers are designed to improve system stability and reference-tracking performance. Static and dynamic precompensators are also considered to reduce tracking error, improve disturbance rejection, and enhance the overall response.

Since all system states may not be directly measurable, full-order and reduced-order observers are designed to estimate the unavailable states.

The controller is then evaluated using estimated states under practical conditions such as measurement noise, actuator saturation, and parameter uncertainty.

A Kalman filter is also implemented to improve state estimation in the presence of noise. Finally, the control system is discretized to support possible digital and real-time implementation.

## Project Objectives

- Develop the nonlinear dynamic model of a quadrotor
- Linearize the system around an equilibrium point
- Obtain the state-space representation
- Analyze open-loop system stability
- Evaluate system controllability
- Evaluate system observability
- Investigate the validity range of the linearized model
- Design a state-feedback controller
- Design an LQR controller
- Improve reference tracking
- Reduce the effect of disturbances
- Design static and dynamic precompensators
- Design a full-order state observer
- Design a reduced-order state observer
- Control the system using estimated states
- Analyze the effect of measurement noise
- Evaluate actuator saturation
- Investigate parameter uncertainty
- Implement a Kalman filter
- Discretize the control system

## Nonlinear System Modeling

The first phase of the project focuses on deriving the nonlinear dynamic model of the quadrotor.

The model describes the relationship between:

- System states
- Control inputs
- Translational motion
- Rotational motion
- Dynamic coupling
- System parameters
- External disturbances

The nonlinear model is used as the main reference for evaluating the accuracy and performance of the designed controllers.

## Linearization

To apply linear control methods, the nonlinear model is linearized around a selected equilibrium point.

The linearized system is represented in state-space form:

```text
x_dot = A x + B u
y     = C x + D u
