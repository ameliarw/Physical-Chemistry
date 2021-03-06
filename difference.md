{% include mathjax.html %}


## Difference Method of Evaluating the TDSE

The difference method is a powerful tool of evaluating the TDSE, or any other differential equation. The benefit of this method is that it allows us to omit the need to evaluate the differential equation (or here the Schrödinger equation) at each time, instead it builds the state $\Psi(x,t)$ at each time from the previous state $\Psi(x,t-\Delta t)$. Therefore, this method saves us a lot of computational power and simplifies the calculation significantly. However, these benefits come with a price. Building each state from the previous, means that each calculation will build on the error of the previous calculation, hence the error will exponentially increase. 

Recall that the time-dependent Schrödinger equation is 
<p align="center"> $H \Psi(x,t)= i \hbar \frac{\partial}{\partial t} \Psi(x,t)$. </p>
Now let’s transition from the time differential $\partial t$ to time difference $\Delta t$ so that 
<p align="center"> $H \Psi(x,t)= i \hbar \frac{\Delta \Psi(x,t)}{\Delta t} $, </p>
where $\Delta \Psi(x,t)=\Psi(x,t+\Delta t)-\Psi(x,t). $

So the TDSE becomes
<p align="center"> $H \Psi(x,t)= i \hbar \frac{\Psi(x,t+\Delta t)-\Psi(x,t)}{\Delta t} .$ </p>
This can be rewritten as
<p align="center"> $\frac{\Delta t}{i \hbar} H \Psi(x,t) +\Psi(x,t) =\Psi(x,t+\Delta t). $ </p>
Recall that the Hamiltonian $H$ is the sum of the kinetic and potential energy operators. The potential energy operator is just a multiplication (or matrix multiplication) and the kinetic energy operator mainly consists of a second derivative operator. Both operators allow us to factor out the wavefunction as follow
<p align="center"> $(\frac{\Delta t}{i \hbar} H +I)\Psi(x,t)=\Psi(x,t+\Delta t), $ </p>
where $I$ is the identity matrix such that $I\Psi(x,t)=\Psi(x,t).$

We can consider the whole entity $(\frac{\Delta t}{i \hbar} H +I)$ as one operator, which is computationally easy to build, that operates on the wavefunction at a certain time $t$ to give us the subsequent wavefunction after a time duration $\Delta t$. 

This is all that is needed to compute the wavefunction of the system at any time we want. We can start with a predefined wavefunction at ($t=0$) $\Psi(x, 0)$ and from there we can track the time evolution at any time $t$. But this is exactly where the error accumulation come in. Say we start with an error $\epsilon$ associated with $\Psi(x, 0)$, every time we advance in time by $\Delta t$ we pick up an extra factor of $\epsilon $ and at some point the calculated value would diverge significantly from the real value and our method does not hold anymore.




[Go back to home page](/README.md)
