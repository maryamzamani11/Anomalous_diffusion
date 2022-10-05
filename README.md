# Anomalous diffusion
In a diffusion process, the observables have stochastic motions which their variance change as follows: 
$$\langle \sigma^{2}=(\langle Y^{2}(t)\rangle - \langle Y(t)\rangle ^{2}) \sim t^{2H}.$$ 
Where $H$ is called the Hurst exponent. In a normal diffusion $H=1/2$, the process is called anomalous when $H$ deviates from $1/2$ [[1]](#1). In the latter case there is a violation from the central limit theorem which could have either of these three reasons; 1) the increments $x(t)=y(t+\Delta)-y(t)$ are not independent for all time differences $\Delta$ (the Joseph effect) [[2,3]](#1). 2) the variance of the increments is infinite (the Noah effect). 3) the increment distribution is non-stationary (the Moses effect).

# Time averaged MSD and the correlation
Let $Y_{i}(t)=\sum_{n=0}^t X_i(n)$, be the cumulative sum of the yearly citation number, for some paper $i$, until the year $t$ after its publication. Here, we study the fluctuations of the citation trajectories, using the Time Averaged Mean Square Displacement (TA-MSD). For a single trajectory (citation history of one particular paper $i$), TA-MSD is given by, \cite{klafter2011first};
\begin{equation}
   \overline{\delta^{2}(\Delta)}=\frac{1}{T-\Delta}\sum_{t'=0}^{t'=T-\Delta}[Y_{i}(t'+\Delta)-Y_{i}(t')]^{2}. 
   \label{TAMSD}
\end{equation}
The above moving average sums the number of citations added for each trajectory, at intervals of duration  $\Delta$, until time $T-\Delta$, and divided by $T-\Delta$. $t=T$ is the maximal measured time in our data, which is $T=34$ years. The ensemble-averaged TA-MSD is: $\langle \overline{\delta^{2}(\Delta)} \rangle= \frac{1}{N} \sum_{i=1}^{N}\overline{\delta_{i}^{2}(\Delta)}$. 
%\begin{equation}\label{EATAMSD}
%  \langle \overline{\delta^{2}(\Delta)} \rangle= \frac{1}{N} \sum_{i=1}^{N}\overline{\delta_{i}^{2}(\Delta)}.
%\end{equation}
In the data analysis, we consider the maximum lag-time as $\Delta=|\frac{T}{3}|$. Recently, the TA-MSD has been shown to scale as  \cite{meyer2018anomalous,aghion2020moses} 
\begin{equation}
  \langle \overline{\delta^{2}(\Delta)} \rangle \sim t^{2H-2J}\Delta^{2J},
  \label{Joseph}
\end{equation}
where $J\in[0,1]$ is called the {\em Joseph} exponent, which is associated with the autocorrelations in the time series. For a random process without long-ranged autocorrelations; $J=\frac{1}{2}$. 
If a process is long-ranged and positively correlated; $\frac{1}{2}<J \leq 1$, and for an anti-correlated process $0<J<\frac{1}{2}$ \cite{mandelbrot1968noah,lim2002self,chen2017anomalous}.




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




