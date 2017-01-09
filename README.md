# Monte Carlo simulations
Some scripts based on Monte Carlo methods.

1. [MC integration](https://github.com/mintDan/MonteCarlo#mc-integration)
2. [Approximate Pi](https://github.com/mintDan/MonteCarlo#mc-calculate-pi)
3. [Buffon's Needle with normal distribution](https://github.com/mintDan/MonteCarlo#buffons-needle-normal-distribution)


## MC integration
The MonteCarlo.py script is a module that can be called from other scripts, and is used in Buffon's needle with normal distributed needles.
The probability is calculated by comparing areas here, so in theory only linearly distributed points can be used, I think. To use different distributions, one must 
use the traditional method as adapted from standard numerical integration. 

![MCint.png](https://github.com/mintDan/MonteCarlo/blob/master/figs/MCint.png)

## MC calculate pi
Compares the amount of points landing inside and outside the circle, which together with the area outside, gives an approximation for pi.
As seen here the result is pi = 2.9.

![MCpi.png](https://github.com/mintDan/MonteCarlo/blob/master/figs/MCpi.png)

##Buffon's Needle Normal Distribution
Instead of using a uniform distribution to throw the needle, here are normal distributed needles. 
Pi can still be calculated explicitly, but an approximation to the probability is used in practice, since the normal distribution in essence goes to +- infinity.
The approximated probability P to land near the lines is given below

![P.png](https://github.com/mintDan/MonteCarlo/blob/master/figs/P.png)

The real value for P will be slightly larger than this, which the obtained values for pi show, since it always overshoots.

![Pi.png](https://github.com/mintDan/MonteCarlo/blob/master/figs/Pi.png)

Where the integral I is given by

![I.png](https://github.com/mintDan/MonteCarlo/blob/master/figs/I.png)

To calculate the probability P, we need to calculate the integral I, and this in itself is done by calling MonteCarlo.py as a module.

![BFint.png](https://github.com/mintDan/MonteCarlo/blob/master/figs/BFint.png)

With these results we can continue to find pi. The result is shown below

![MCbuffon.png](https://github.com/mintDan/MonteCarlo/blob/master/figs/MCBuffonGauss.png)
