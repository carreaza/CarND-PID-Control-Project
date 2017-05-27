May 2017
Carlos Arreaza

Reflection on CarND-Pid-Projec

1) Student describes the effect of the P, I, D component of the PID algorithm in their implementation. Is it what you expected?

Proportional: this takes care of the curent amount of error. If the current error is big, the correct will be proportionally big. If the current error is small, the correction will be proportionally small. Usually P increases the amount of overshoot in the system and decreases the rise time and steady state error.

Derivative: this takes care of the change in error with respect to time. If the error is changing quickly, then the correction will tend to be bigger, however is the error is changing very slowly, there will be a very small correction. The D term tends to decrease the overshoot in the system, however it doesn't eliminate the steady state error.

Integral: this takes care of the cumulative error that happens over time. Thus, the I term tends to get rid of the steady state error.



2) Student discusses how they chose the final hyperparameters (P, I, D coefficients). This could be have been done through manual tuning, twiddle, SGD, or something else, or a combination!

The hyperparameters were chosen manually following a very simple strategy: first focus on the P, while I = D = 0. The number 0.2 was chosen as it had the least amount of steady state error. Then, D was introduced to get rid of the high overshoot. the number between 0.00015-0.0002 was chosen as it showed a reduction in the overshoot. Finally, the integral term was introduced to get rid of the steady state error. I = 2 was chosen as it gave the best performance on the vehicle.
