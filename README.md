# CarND-Controls-PID
Self-Driving Car Engineer Nanodegree Program

---

## About PID Controller Implemented
PID controller is widely used for obtaining a desired state. In this project the desired state is to follow the lane with minimum cross track error and the control variable is the steering angle

PID controller changes the control variable, the steering angle in proportion to cross track error, its integral parts and differential part


```
d_error = cte - p_error;
p_error = cte;
i_error += cte
Steering_Angle = -Kp * p_error - Ki * i_error - Kd * d_error;
```

## How it is tuned
I used twiddle to obtain Kp, Ki and Kd. The parameters I obtained didnt quite work well. Then I started to manually fine tune things based on the vehicle behaviour in the simulator. The manual tuning is done as follows

* If the steering value is high even for small cross track error, I decreased Kp and vice versa
* If the steering value is not decreasing as the cross track error dereases, I increased Kd and vice versa
* In steep turns, where some times Integral component will Kick in if proportional component is insufficient, I tuned Ki accordingly.

From my tuning I observed that the controller performs almost the same for wide reange of combinations of Kp, Kd, Ki



