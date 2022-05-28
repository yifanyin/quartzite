---
title: "Dieterich.JGR.1994.stress2rate"
tags:
- reference
- JGR
- seismicity
---

# A constitutive law for rate of earthquake production and its application to earthquake clustering
- Authors: [[notes/James H Dieterich|James H Dieterich]]
- [Source](https://agupubs.onlinelibrary.wiley.com/doi/abs/10.1029/93JB02581)
# Notes
The essential concept of the analysis is the treatment of a seismically active volume of the Earth as having a population of sources that nucleate successive earthquakes to produce observed seismicity. The objective is to find the time at which each source in the population initiates an earthquake by following the evolution of conditions on the sources when subjected to some stressing history.

   - Here the volume containing the sources is assumed to be small enough to undergo the same stressing history.
   - The time of nucleation $t = F[C, \tau(t)]$. C is the initial condition and $\tau(t)$ is the stressing history.
   - At each time step, C is reevaluated using the prior stressing history and the state distribution.

Assume the initial condition is under a reference constant stressing rate $\dot\tau_r$ and generate constant seismicity rate $r$
- The time when $n^{th}$ event occur: $$t = n/r = F[C, \tau_r] \tag{1;2}$$
- So, $C = C(n, r, \dot\tau_r)$ (3)
- and $t = F[C(n, r, \dot\tau_r), \tau(t)]$ (4)

## Rate-and-state friction incoming
- [[Dieterich.Tectonophysics.1992]]
- Link the [[notes/rate-and-state friction|rate-and-state friction]] using $\tau$

$$\tau=\sigma[\mu_0+A\ln(\frac{\dot\sigma}{\dot\sigma^*})+ B_1\ln(\frac{\theta_1}{\theta^*_1})+B_2\ln(\frac{\theta_2}{\theta^*_2})+...] \tag{5}$$

$$d\theta_i = [\frac{1}{\dot\delta} - \frac{\theta_i}{Dc}]d\sigma - [\frac{\alpha_i\theta_i}{B_i\sigma}]d\sigma$$

State change with 1. aging law and 2. normal stress law from Linker and Dieterich, 1992.

## Appendix A: Earthquake nucleation
The author reiterates the $L_c$ and said empirical evaluation of the size of the nucleation zone from the numerical models gives $\xi$ ~ 0.4B.

Simulations of faults with heterogeneous properties show that:
- The zone of most rapid acceleration tends to shrink to a characteristic fault length of $L_c$ (Appendix A, equation (A2)) as the time of instability approaches.
- Nucleation sources of length $L_c$ develop spontaneously in regions where the shear stress relative to the sliding resistance averaged over $L_c$ is higher than the surroundings.

In general, slip speed is determined by the independent variables $\theta$, $\tau$, and $\sigma$. It is shown in Appendix A that in an accelerating slip patch evolution of $\theta$ is determined by slip. Under this condition, the dependence of the time to instability on initial conditions is fully specified by the initial slip speed ${\dot\delta}_0$ of the patch (Appendix A, equation (A7)).

$$\dot\delta_0 = (\theta_{o_1}^{-B_1/A}\theta_{o_2}^{-B2/A}...)exp(\frac{\frac{\tau_0}{\sigma}-\mu'_0}{A}) \tag{A7}$$

The distribution of initial slip speed is (7). The form remains when time progress.
$$\dot\delta(n) = [H\sigma\gamma(exp(\frac{\dot\tau_r n}{A\sigma\tau})-1)]^{-1} \tag{7}$$

$$H = \frac{B}{D_c} - \frac{k}{\sigma}$$ ^ZBlaLBaW9

Initially, $$\gamma = \frac{1}{\dot\tau_r} \tag{8}$$ where $\tau_r$ is the reference shear stress. $\gamma$ is a state variable that evolves with time and stressing history. Essentially, the seismicity rate is controlled only by the stressing rate.

The state variable evolves with time as

$$d\gamma = \frac{1}{A\sigma}[dt - \gamma d\tau + \gamma(\frac{\tau}{\sigma} - \alpha)d\sigma] \tag{9}$$ ^Dieterich1994-9

- The steady-state solution goes back to (8)
- $A$ generally has values between 0.005-0.012 ^jN7GXVW6b
- These equations reproduce Omori's law of aftershock decay with 1/time.
- At steady state
$$\gamma_{ss} = \frac{1}{\dot\tau}; t_a = \frac{A\sigma}{\dot\tau} \tag{10}$$
- Seismicity rate $R = \frac{r}{\gamma\dot\tau_r}$. $r$ is the reference seismicity rate. (11) ^eSoqds2k-
- So at steady state, the rate ratio equals the ratio of shear stressing rate.

==How does the seismicity rate change following a stress step?==

## Equations
The seismicity rate change with respect to time after a stress step:
$$R = \frac{r\frac{\dot\tau}{\dot\tau_r}}{[\frac{\dot\tau}{\dot\tau_r}\exp{\frac{-\Delta\tau}{A\sigma}}-1]\exp{\frac{-t}{t_a}}+1}, \dot\tau \neq 0. \tag{12}$$

Recall Omori-Utsu law: $R = \frac{a}{b+t}$
Although different from the more general form of [[notes/statistical seismology#Omori-Utsu law|Omori's Law]]

### Aftershock duration or characteristic relaxation time
$$t_a = \frac{A\sigma}{\dot\tau} = \frac{A\sigma}{-\Delta\tau_e} \tag{14}$$
$\Delta\tau_e$ is the stress change of the event. ^g5xSByqSw

A formulation for the effect of stressing history on earthquake rate
![[Dieterich.JGR.1994.stress2rate#^Dieterich1994-9]] (B14)