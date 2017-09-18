# CarND-Controls-PID
Self-Driving Car Engineer Nanodegree Program

---

## About PID Controller Implemented
PID controller is widely used for obtaining a desired state. In this project the desired state is to follow the lane with minimum cross track error and the control variable is the steering angle

PID controller changes the control variable, the steering angle in proportion to cross track error, its integral parts and differential part


`
d_error = cte - p_error;
p_error = cte;
i_error += cte
Steering_Angle = -Kp * p_error - Ki * i_error - Kd * d_error;
`



