# Anomalous diffusion
In a diffusion process, the observables have stochastic motions which their variance change as follows: 
$$\sigma^{2}=(\langle Y^{2}(t)\rangle - \langle Y(t)\rangle ^{2}) \sim t^{2H}.$$ 
Where $H$ is called the Hurst exponent. In a normal diffusion $H=1/2$, the process is called anomalous when $H$ deviates from $1/2$ [[1]](#1). In the latter case there is a violation from the central limit theorem which could have either of these three reasons; 1) the increments $X(t)=Y(t+\Delta)-Y(t)$ are not independent for all time differences $\Delta$ (the Joseph effect) [[2,3]](#1). 2) the variance of the increments is infinite (the Noah effect). 3) the increment distribution is non-stationary (the Moses effect)[[1]](#1).

# Time averaged Mean Square Displacement (MSD) and the correlation
Let; $$Y_{i}(t)=\sum_{n}^t X_i(n)$$, be the cumulative sum of the increments, for trajectory $i$ (imagine we have an ensemble of the trajectories), $t$ is time. 
So, $Y_{i}(t)$ could be any types of trajectories. Here in this repository, I looked for the fluctuations of the citation time series, but you can apply this to other process as well like stock prices if you have an ensemble of different stocks. 
The Time Averaged Mean Square Displacement (TA-MSD) for a single trajectory is given by, [[4]](#1);
 $$\overline{\delta^{2}(\Delta)}=\frac{1}{T-\Delta}\sum_{t'=0}^{t'=T-\Delta} (Y_{i}(t'+\Delta)-Y_{i}(t'))^{2}.$$
 
 The overline means time-average, $t=T$ is the maximal measured time, which in our dataset is $T=34$ years. The ensemble-averaged TA-MSD is:

$$\langle \overline{\delta^{2}(\Delta)} \rangle= \frac{1}{N} \sum_{i=1}^{N}\overline{\delta_{i}^{2}(\Delta)}.$$

where, angled brackets mean ensemble average, in the data analysis, we consider the maximum lag-time as $\Delta=|\frac{T}{3}|$. It has been shown that the TA-MSD scales as [[1]](#1): 

$$  \langle \overline{\delta^{2}(\Delta)} \rangle \sim t^{2H-2J}\Delta^{2J},$$

where $J\in[0,1]$ is called the Joseph exponent, which is associated with the autocorrelations in the time series. For a random process without long-ranged autocorrelations; $J=\frac{1}{2}$. If a process is long-ranged and positively correlated; $\frac{1}{2} < J <= 1$, and for an anti-correlated process $0 < J < \frac{1}{2}$ [[2]](#1).

## Nonstationarity and the Moses exponent

in a stochastic process $Y_{t}$, if the probability distribution of the increments $(Y(t+\tau)-Y(t))$ is independent of $t$, the increments are considered stationary. In Refs.[[1]](#1), it was shown that the level of non-stationarity can be quantified by a single parameter, which is called the Moses exponent. This parameter can be measured directly from the data. The Moses exponent $M$ is defined with the temporal scaling of the enseble average of the time series, of the sum of the absolute value of increments of the process. We can obtain the Moses exponent from:  
$$\langle Y(t) \rangle \sim t^{M+\frac{1}{2}}.$$
For normal diffusive processes, with stationary increments; $M=1/2$. For nonstationary process, when the process dies out since its increments become smaller in time; $M$ is smaller than $1/2$. When $M>1/2$, it indicates that the absolute-increments grow in time.

## The significance of large, rare fluctuations; the Noah effect

In time-series analysis, when we do not have a large ensemble of data to obtain clear statistics from, the influence of fat-tails in the increment distribution of the process on the anomalous diffusion, can be measured directly \textbf{from a small number of sufficiently long paths}, with the so-called "Noah effect". The Latent exponent $L$ can be found from:

 $$\langle Z_{t}\rangle = \langle \sum_{s=1}^{t} X_{i}(s)^{2} \rangle \sim t^{2L+2M-1}.$$ 

Note that, here I wrote a sampled ensemble average, which is guaranteed to have a finite value at finite times, as opposed to the theoretical value which will be divergent if the increment distribution has scale-free fat tails. One can also use the sampled-median here, instead of the mean. 
When $M=1/2$, we do not observe aging effects in the time-series, if $L=1/2$; $\langle Z_{t}\rangle \sim t$, which is similar to a standard Gaussian process with a finite increment-variance. On the other hand, when $L>1/2$, this can only occur because the increment distribution at least has a regime, with a power-law shape that falls-off as $1/C^\gamma$, and $0<\gamma<2$ [[1,2]](#1). In this regime the distribution does not have a typical value. This power-law shape of the tails of the distribution might have a time-dependent cutoff, which is pushed towards $\infty$ as time increases.

## Hurst exponent

The Hurst exponet which can be found from the variance of the process (the first equation above), it was shown that using the three exponents; $M,L$ and $J$, we can obtain the Hurst exponent with a simple summation relation. 
$$H=J+L+M-1.$$

You can read the explanation of all the figures that I found in this code in ref.[[6]](#1). 

 ## References
 <a id="1">[1]</a>
 Chen, Lijian and Bassler, Kevin E. and McCauley, Joseph L. and Gunaratne, Gemunu H. (2017)
 Anomalous scaling of stochastic processes and the Moses effect.
 Phys. Rev. E, 95, 042141.

 <b id="2">[2]</b>
 Mandelbrot, Benoit B and Van Ness, John W. (1968)
 Fractional Brownian motions, fractional noises and applications.
 SIAM review, 10, 422--437.

 <c id="3">[3]</c>
 Graves, T. and Gramacy, R. and Watkins, N. and Franzke, C. (2017)
 A Brief History of Long Memory: Hurst, Mandelbrot and the Road to ARFIMA, 1951-1980.
 Entropy, 19(9), 437.

 <d id="4">[4]</d>
 Klafter, Joseph and Sokolov, Igor M. (2011)
 First steps in random walks: from tools to applications.
 Oxford University Press.

<e id="5">[5]</e>
Meyer, Philipp G and Adlakha, Vidushi and Kantz, Holger and Bassler, Kevin E. (2018)
Anomalous diffusion and the Moses effect in an aging deterministic model.
New Journal of Physics, 20(11), 113033.

<e id="6">[6]</e>
Zamani, Maryam and Aghion, Erez and Pollner, Peter and Vicsek, Tamas and Kantz, Holger. (2021)
Anomalous diffusion in the citation time series of scientific publications.
Journal of Physics: Complexity, 2(3), 035024.





