---
{"dg-publish":true,"dg-home":true,"permalink":"/membrane-potential/rc-circuit/","tags":["gardenEntry"],"dgPassFrontmatter":true}
---


- Rm: Pooled conductance of the cell membrane 
- [[Membrane Potential/Equivalent Components#Membrane Capacitance\|Cm]]: capacitance of the entire membrane 
![Pasted image 20250909211533.png](/img/user/Image/Pasted%20image%2020250909211533.png)
- When current is injected, it flows either through the resistor or into the capacitor 
	- current cannot flow *through* capacitor 
- [[Membrane Potential/Electrical Components and Circuit#Capacitance (C)\|current flow into the capacitance is proportional to the rate of change of membrane voltage]]
	- Beginning (high rate): *all current* flows into the capacitor 
	- voltage across the circuit increase in proportion to the amount of charge transferred to the capacitor 
		$$V_{m} = \frac{q}{C_{m}}$$
- *Increase in Vm* → increase fraction of current *flowing through the resistor* 
	- expected from Ohm's law 
	
<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



- describes the linear relationship between voltage and current for and ideal resistor 
	$I = \frac{V}{R} = GV$

</div></div>

- **Current flow through the resistor is directly parallel to the changes in voltage** 
	- if the current is sustained → rate of change of voltage falls to zero 
		- no capacitive current only a resistive current 
	- At the *offset* of current step, charge stored on the capacitor flows through the resistor to ground 
		- *voltage declines slowly until all the charge has left the capacitor* 

> [!Example] [[Membrane Potential/Electrical Components and Circuit#Kirchhoff's law\|Kirchhoff's Law]]
> $$
\begin{aligned}
I_{m} &= I_{R}+I_{C} \\
I_{R} &= \frac{V_{m}}{R_{m}} (Ohm's \space law) \\
I_{C} &= C_{m} \frac{dV_{m}}{dt} (capacitance)\\
\tau_{m} &= R_{m}C_{m} \\
\tau_{m}\frac{dV_{m}(t)}{dt} &= -V_{m}(t)+R_{m}I_{m}(t) \\
\end{aligned}
$$

> [!Note] Time constant (Tm)
> $$\tau_{m} =R_{m}+C_{m}$$
> - ***$\tau_{m}$ is proportional to resistance and conductance***
> - the time when the voltage reaches **0.63 of $V_{\infty}$** 
> - determines the rate of change of the voltage 
>	-  if current injected at t = 0, change in voltage: 
>		$$ V_{m}(t) = V_{\infty}(1-e^{-t/\tau_{m}}) $$
>	- At the offset of the current step, the change in voltage: 
>		$$ V_{m}(t)= V_{\infty}e^{-{t}/{\tau_{m}}} $$
>- ***mitigated by a variety of factors*** 
>	- complex geometry of neurons → reduce the effective time constant 
>	- synchronous synaptic activity → reduce Cm and Tm 
>	- active conductances in dendrites → amplify the response to synaptic inputs 

### Filtering effect of RC circuit 
- *large membrane capacitance* is a ***significant constrain*** on speed of electrical communication between neurons 
- A circuit acts as a low-pass filter 
	- block high frequency signals 
	- allows lower frequency signal to pass 
	![Pasted image 20250909222246.png](/img/user/Image/Pasted%20image%2020250909222246.png)
- membrane capacitance sets a minimum duration for the current signal 
	- **filter effect** : electrical signaling between cells is many orders of magnitude slower than signaling within conventional electronic circuits 