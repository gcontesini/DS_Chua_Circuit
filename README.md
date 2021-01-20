
# DS_Chua_Circuit

Similate the Chua Circuit, [insert theory and background bibliography here]


The entire system and analysis was based the Sordi A. paper. [see ref.]


The reason why I did this was that I just found this system very interest.

System Differential Equation ( dimensionless )

- <img src="https://latex.codecogs.com/gif.latex?\frac{d}{dt}x=\alpha[y-x(b+1)-f(x)]\>

$\frac{d}{dt}y = x-y+z$

$\frac{d}{dt}z = -\beta y+\epsilon z$

and  input current $f(x)$

$f(x)=a \tanh(\phi x)$

## Parameters

$a= -0.428$
$b= -0.614$
$\phi = 2.0$
$\alpha = 9.0$
$\beta = 15.0$
$\epsilon = 0.125$

## Method

Simpletic Runge-Kutta of 4 order

### Global Conditions

time_step = 0.01

### Initial Conditions

$x_0 = 0.15$
$y_0 = 0.15$
$z_0 = 0.15$

for the Lyapunov calculation a $\delta=1e^{-6}$ was add to the original IC.

## Results 

![original Chua attractor](https://github.com/gcontesini/DS_Chua_Circuit/blob/master/ts_chua_circuit.png)

![x time series](https://github.com/gcontesini/DS_Chua_Circuit/blob/master/chua_circuit_x_ts.png)

![y time series](https://github.com/gcontesini/DS_Chua_Circuit/blob/master/chua_circuit_y_ts.png)

![z time series](https://github.com/gcontesini/DS_Chua_Circuit/blob/master/chua_circuit_z_ts.png)

![Lyapunov Exponent](https://github.com/gcontesini/DS_Chua_Circuit/blob/master/chua_circuit_lyapunov_exp.png)

With a lyapunov exponent of $0.132756$ and a Lyapunov time of $7.5357$, after 
60 interactions delta becames stochastic.[note that de plot is on a y-semi-logscale]

## Stability Points

The Stability points can be achieve by open the circuit

$i^{\star}(x)= -x\cdot(\frac{\epsilon}{(\beta+\epsilon)}+b)$

When the circuit is open, the current
First Stable Points$x=1.1686\hspace{0.25cm}  y=0.0096\hspace{0.25cm}  z=-1.1589$

$x=-1.1686\hspace{0.25cm}  y=-0.0096\hspace{0.25cm}  z=1.1589$

![First Stable Point](https://github.com/gcontesini/DS_Chua_Circuit/blob/master/ts_chua_circuit_FSP.png)

![Second Stable Point](https://github.com/gcontesini/DS_Chua_Circuit/blob/master/ts_chua_circuit_SSP.png)

## Taken's Theorem

Reconstruction of the Lorenz attractor based on taken's theorem

The lag was no optimized so these plots can have way more information.

This is black magic for sure! That is much more one can extract from Taken's Theorem, but I'm lazy go read some classical dynamical system papers.

![only x time series](https://github.com/gcontesini/DS_Chua_Circuit/blob/master/chua_x_takens_theorem.png)

![only y time series](https://github.com/gcontesini/DS_Chua_Circuit/blob/master/chua_y_takens_theorem.png)

![only z time series](https://github.com/gcontesini/DS_Chua_Circuit/blob/master/chua_z_takens_theorem.png)

## Reference

![wiki](https://en.wikipedia.org/wiki/Chua%27s_circuit)

![Alexandre Sordi paper](https://doi.org/10.1590/1806-9126-rbef-2020-0437)

![L.O. Chua](https://arxiv.org/abs/1710.02677)


