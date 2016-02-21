#Difference Equasions

##Linear Difference Equasion

The linear difference equation has the form:

$$y_{n+1} = ay_n + b$$

The general solution for y<sub>n</sub> is:

$$y_n=\frac{b}{1-a} + (y_0- \frac{b}{1-a})a^n$$


###Long term behaviour

| Type of behaviour | Indicator | Condition  | Behavior |
|-------------------|-----------|------------|----------|
| Vertical behavior | Sign of a | a > 0      | Solution monotone
|||a < 0| Solution oscillating
| Long term behavior| Sign of a | lal < 1  | Attracted to equilibrium|
||| lal > 1 | Repelled by equilibrium |
##Logistic Difference Equation

The logistic difference equasion has the form:

###Theorem 2

$$y_{n+1}=y_n + ry_n(M-y_n)$$
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