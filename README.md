In this project, I implemented a **longitudinal PID** and **lateral Stanley controller** to drive an ego vehicle around a given set of waypoints in the Carla simulator. 

The PID controller simulates the following model: <br>
<img width="497" alt="Screen Shot 2022-06-16 at 6 27 46 PM" src="https://user-images.githubusercontent.com/90004171/174204111-60935f20-fe3f-4eb5-84ae-92b575589075.png">

where Kp, Ki, and Kd are the proportional, integral, and derivative gains, respectively. The error term is defined as the difference between the desired velocity and the current velocity: e (t) = v_desired (t) - v (t). The output of the controller is the throttle input for the subsequent timestep, defined as a percentage between 0.0 and 1.0. Finally, I manually tuned the PID controller considering the following behaviors from independently manipulating each of the constant gains: 

<br>
<img width="687" alt="Screen Shot 2022-06-16 at 6 34 02 PM" src="https://user-images.githubusercontent.com/90004171/174204746-bc3aca57-1e0a-435f-a84a-3ad7494b39d9.png">

The Stanley controller is employed to output approrpriate steering commands that keep the ego vehicle on its expected path. The Stanley method uses the center front axle of the vehicle as its reference point and the follow kinematic model: 

<br>
<img width="643" alt="Screen Shot 2022-06-16 at 6 36 09 PM" src="https://user-images.githubusercontent.com/90004171/174204940-ff709a6c-2fe5-412d-8940-84193b36737f.png">

where δ is the steering angle, e is the crosstrack error, and ψ is the heading error. 
