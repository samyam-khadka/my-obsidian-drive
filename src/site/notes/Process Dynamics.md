---
{"dg-publish":true,"dg-home":true,"permalink":"/process-dynamics/","tags":["gardenEntry"],"dgPassFrontmatter":true}
---

## Tutorial 1
- Cd = 1 (unless otherwise stated)
- Torricelli’s Law: 
	$$ v = \sqrt{ 2gh } $$
- Flow rate out = 
	$$ -Cd \cdot Ac \cdot v $$
	* Note: Ac is the area of the cross-sectional area of the hole/ exit.

* $$ \frac{dV}{dt} = A(y) \cdot \frac{dy}{dt}$$
	* Note: A(y) is the cross-sectional area given changing y. Different from Ac. Will be a function that depends on y.
- For water that's decreasing over time, y integration has 0 at the top and full height at the bottom (as a positive value).
- For initial height (draining question) 90% full initially means 0.9 x height of tank.

## Tutorial 2
- Assume tank (even if multiple components are coming in) has constant density.
- Assume the tank is well mixed.
- Due to well mixed assumption 
	$$\frac{d(V \cdot \rho \cdot x)}{dt} = F_{in} \cdot x -F_{out} \cdot x +Generation - Consumption$$ the '**x**' is the same as the concentration of the outflow.
	- The concentration x of the component inside the system is the same everywhere in the system.
* @ steady-state anything over dt with equal to 0 (as process variables do not change over time).
* **constant liquid holdup** means the V = cte. dV/dt = 0.
	* even if say w1 value changes for example, this is still cte.
* ![CleanShot 2025-02-18 at 20.34.28@2x.png](/img/user/Images/CleanShot%202025-02-18%20at%2020.34.28@2x.png)
	* Determine an expression for x(t) means use tau and k.
	* Also, we need to understand we are modelling the x change that occurs from steady state in a until a new steady state is reached in b.
		* So, initial condition is technically defined x(0) = x @ steady state in a.

* Integration Factor approach:
		$$\begin{gathered} \frac{dy}{dt} + P \cdot y = Q  \\ e^{\int Pdt}\frac{dy}{dt} + P \cdot e^{\int Pdt} \cdot y = e^{\int Pdt} \cdot Q \\ \int d\left( y \cdot e^{\int Pdt} \right) = \int Q \cdot e^{\int Pdt} dt \\ y \cdot e^{\int Pdt} = \int Q \cdot e^{\int Pdt} dt \end{gathered}$$
## Tutorial 3
* Read Laplace Table using the f(t) value (e^-st) doesn't matter.
* After doing partial fraction, we can take each component of the partial fraction as individual thing in Laplace table when doing Laplace inverse.
	* Laplace properties: 
		 $$ \mathscr{L}(f(t) + g(t)) = \mathscr{L}(f(t) ) + \mathscr{L} (g(t)) $$
* By definition: Step input --> suddenly changes from 0 to certain value at certain time and remains such forever (otherwise defined).
* I have no clue why I forgot the most basic thing: 
		$$ \begin{gathered}
\mathscr{L}(f(t)) = F(s) \\ \mathscr{L'}(F(s)) = f(t)
\end{gathered}$$

## Tutorial 4
