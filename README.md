# Learning Barrier Certificates for Neural Path Tracking Control of Self Driving Vehicles - Extension

An extension of paper *Learning Barrier Certificates for Neural Path Tracking Control of Self Driving Vehicles* is contained in the [PDF file](./Quantifying_Safety_of_Learning-based_Self-Driving_Control_Using_Almost_Barrier_Functions_Supplementary_Materials.pdf), with the following sections

1. Pseudocodes
2. Policy Learning
3. Learning Low-Dimensional Barriers under Partial Observability
4. Estimating Range of Dynamics near Samples
5. Finding Boundary Counterexamples for Retraining
6. Using the Learned Barrier Function for Safety Monitor
7. Hyper-parameters and Details of Experiments


Below we present figures contained in the original and extended paper.

---


## Pseudocodes

### Training the Barrier Function

<p align="center">
  <img src="figures/pseudocodes_training.png">
</p>

### Cerifying the Barrier Function

<p align="center">
  <img src="figures/pseudocodes_certification.png">
</p>


## Dynamic Model Trajectories Illustration

Plotting of trajectories of the dynamic model, with x, y axes as angle and distance errors, and z axis as:

Longitudinal Speed         |  Lateral Speed           | Yaw Rate
:-------------------------:|:------------------------:|:-------------------------:
![Dynamic Model Trajectory Longitudinal Speed](/figures/dynamic_trajectories_longitudinal_speed.png)  |  ![Dynamic Model Trajectory Lateral Speed](/figures/dynamic_trajectories_lateral_speed.png)  | ![Dynamic Model Trajectory Yaw Rate](/figures/dynamic_trajectories_yaw_rate.png) 

---

## Flow Chart of Overall Pipeline

<p align="center">
  <img src="figures/flow.png">
</p>

---

## Vehicle Dynamics Models

Kinematic Model      |  Dynamic Model    
:-------------------------:|:------------------------:
![Kinematic Model](/figures/kinematic_model.png)  |  ![Dynamic Model](/figures/dynamic_model.png) 

---

## Barrier Functions

The barrier functions on kinematic model, dynamic model and TORCS environment

Kinematic Model (3D)       |  Dynamic Model (2D)      | TORCS (2D)
:-------------------------:|:------------------------:|:-------------------------:
![Kinematic Barrier](/figures/barrier_kinematic_model.png)  |  ![Dynamic Barrier](/figures/barrier_dynamic_model.png)  | ![TORCS Barrier](/figures/barrier_TORCS.png) 

---

## Safety Monitor

Backward reachable states for dynamic model, evaluated on a maximum curvature of 0.15, for 50 time steps


Path with Curvature 0.15 (Curve to Left)   |  Path with Curvature 0.15 (Curve to Right)       | Safety Monitor
:-------------------------:|:------------------------:|:-------------------------:
![Kinematic Barrier](/figures/curve_course_0.15.png)  |  ![Dynamic Barrier](/figures/curve_course_-0.15.png)  | <p align="center"> <img width="350" src="figures/monitor.png"></p>

---

## Importance of Retraining

The barrier function for dynamic model obtained after the initial training and after the final retraining, projected in the dimensions of angle and distance error

Initial Barrier      |  Final Barrier     
:-------------------------:|:------------------------:
![Retraining Initial Barrier](/figures/retraining_initial_barrier.png)  |  ![Retraining Final Barrier](/figures/retraining_final_barrier.png) 

---

## Vector Fields of Dynamic Model

Close to Collected Trajectories      |  Whole Certification Grid     
:-------------------------:|:------------------------:
![Vector Field Close](/figures/vector_field_dynamic_model_close.png)  |  ![Vector Field Whole Grid](/figures/vector_field_dynamic_model_whole.png) 

---

## Barrier Behavior of TORCS Environment

<p align="center">
  <img width="400" src="figures/TORCS_barrier_behavior.png">
</p>