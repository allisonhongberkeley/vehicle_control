In this project, I implemented a longitudinal PID and lateral Stanley controller to drive an ego vehicle around a given set of waypoints in the Carla simulator. 

The PID controller simulates the following model: 
<img width="497" alt="Screen Shot 2022-06-16 at 6 27 46 PM" src="https://user-images.githubusercontent.com/90004171/174204111-60935f20-fe3f-4eb5-84ae-92b575589075.png">

where Kp, Ki, and Kd are the proportional, integral, and derivative gains, respectively. The error term is defined as the difference between the desired velocity and the current velocity: e (t) = v_desired (t) - v (t). The output of the controller is the throttle input for hte subsequent timestep, defined as a percentage between 0.0 and 1.0. 

