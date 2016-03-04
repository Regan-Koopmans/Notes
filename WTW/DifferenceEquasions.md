
#Difference Equasions

##Linear Difference Equasion

The linear difference equation has the form:

$$y_{n+1} = ay_n + b$$

The general solution for y<sub>n</sub> is:

$$y_n=\frac{b}{1-a} + (y_0- \frac{b}{1-a}).a^n$$


###Long term behaviour

| Type of behaviour | Indicator | Condition  | Behavior |
|-------------------|-----------|------------|----------|
| Vertical behavior | Sign of a | a > 0      | Solution monotone
|||a < 0| Solution oscillating
| Long term behavior| Sign of a | lal < 1  | Attracted to equilibrium|
||| lal > 1 | Repelled by equilibrium |

An equilibrium will be found at the point:
$$k = \frac{b}{1-a}$$

####==Special Cases==

1. If $$$y_{n+1}=y_n+b$$$ then there is no equilibrium.
2. If $$$y_{n+1}=ay_n$$$ then the equilibrium is $$$y=0$$$

##Logistic Difference Equation

The logistic difference equasion has the form:

$$y_{n+1}=y_n + ry_n(M-y_n)$$

Where the initial value $$$y_0$$$ is given and $$$M$$$ represents the carrying capacity.


###Theorem 2

so...
$$\Delta y = ry_n(M-y_0)$$
$$\frac{\Delta y}{y_n} = r(M-y_0)=rM-ry_0$$
but...
$$\frac{\Delta y}{y_n}=ay_n+b$$
so...
$$a=-r ,\space\space b=rm$$

###Theorem 3

$$Let \space \frac{1}{r} < M < \frac{2}{r} \space $$

1. There exists 2 equilibria y = 0 and y = m.
2. If y<sub>0</sub> &ge; M + 1/r ,then y<sub>1</sub> &le; 0.
3. If 0 &lt; y<sub>0</sub> &lt; M + 1/r, then y<sub>n</sub> tends to equilibrium M as n increases.
4. The population will start oscillating as soon as y<sub></sub> &gt; 1/r

###Constructing a Logistic Difference Equasion from Data

Recall that the relative growth for a logistic difference equasion is:

$$\frac{\Delta y_n}{y_n}=ay_n+b_n$$

where $$$a=-r$$$ and $$$b=rM$$$

==This way when we construct a line through the data and reveive an *a* and *b* we can convert them back to r and M.==

##Other Difference Equasions

$$y_{n+1}=r(y_n)y_n$$
where $$$r(y_n)$$$ is the growth factor.
Equilibria are obtained by setting $$$r(y)=0$$$

##Systems of Difference Equasions