# Anomalous diffusion
In a diffusion process, the observables have stochastic motions which its variance change as follows: 
$\langle y^2(t) \rangle \sim 2Dt^H$

Typically the values
of the observables are unbounded, such that the expected squared displacement
grows with time. If the stochastic forces are such that the
central limit theorem can be applied, then the accumulated fluctuations scale
with the square root of time:

where $H=1/2$, called normal diffusion. However, the exponent $H$ might deviate
from $1/2$ if one of the three premises of the central limit theorem is
violated \cite{Che17}, namely if the increments $x(t)=y(t+\Delta)-y(t)$ are not
independent for all time differences $\Delta$ (the Joseph effect)
\cite{Man68fbm,Wat17}; if the variance of the increments is infinite (the Noah
effect); or if the increment distribution is non-stationary (the Moses
effect). In the latter case, anomalous diffusion with some exponent
$H\neq 1/2$ results if the variance of the increments
scales with a power law in time. Here, the
paradigmatic model is scaled Brownian motion \cite{Jeo14}. In contrast to
this, the exponent remains $H=1/2$ in the long time limit in case of,
e.g., periodic non-stationarities, since a longer temporal spacing would
eliminate the non-stationarity.
