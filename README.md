# Step7_v5.6
The projects here are about the PLC programing 

PDI Controller, useful in PLC, S7 200 300 400 Siemens: 
    This block is a Discrete PID Controller, that is, instead of being with respect to time, it is with respect to error samples, where the sampling has a period in the time.

    To get the control action (Un): error (en)
    samples (kn)
    Sampling time = T
    Un (t) = kp * in (t) + (ki * integral (in (t))) + (kd * derivative (in (t)))
    T = Kn-Kn_1
    Discrete integral: integral (in (kn)) = in (kn) * T + in (kn_1)
    Discrete derivative: derivative (in (kn)) = (in (kn) -en_1) / T

    The last block of MOVE.
    It is to assign en => en_1 (The present error goes to the past error)
