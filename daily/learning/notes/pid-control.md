# PID Control

连续控制系统中理想的PID控制规律：

$$
u(t)=K_p(e(t)+\frac{1}{T_t}\int^{t}_{0}e(t)dt+T_D\frac{de(t)}{dt})
$$

离散算法：

$$
u(t)=K_pe(t)+K_i\sum^{t}_{i=0}e(i)+K_d(e(t)-e(t-1))
$$

