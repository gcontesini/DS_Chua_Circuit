
# DS_Chua_Circuit

Similate the Chua Circuit, [insert theory and background bibliography here]


The entire system and analysis was based the Sordi A. paper. [see ref.]


The reason why I did this was that I just found this system very interest.

System Differential Equation [ adimentional ]

$\frac{d}{dt}x = \alpha[ y - x(b+1) - f(x)]$

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

![original Lorenz attractor]()

[x ts]()

[y ts]()

[z ts]()

[Lyapunov Exponent]()

With a lyapunov exponent of $0.132756$ and a Lyapunov time of $7.5357$, after 
60 interactions delta becames stochastic.[note that de plot is on a y-semi-logscale]

## Stability Points

The Stability points can be achieve by open the circuit

$i^{\star}(x)= -x\cdot(\frac{\epsilon}{(\beta+\epsilon)}+b)$

When the circuit is open, the current
$x=0.6104\hspace{0.25cm}  y=0.0050\hspace{0.25cm}  z=-0.6053$

## Taken's Theorem

Reconstruction of the Lorenz attractor based on taken's theorem

This is black magic for sure! That is much more one can extract from Taken's Theorem, but I'm lazy go read some classical dynamical system papers.



## Reference

[Alexandre Sordi paper](https://doi.org/10.1590/1806-9126-rbef-2020-0437)
