# Homework

These are the recommended homework problems for the topic of Bending. We highly recommentd you follow the IDEA framework (see {numref}`fig_IDEA`) for approaching the solution of each problem. Write out your steps in this approach such that you can easily show a colleague and they could check your work. Effective communication of your solution is arguabbly more valaubale then getting the correct answer!

```{warning} Calculator/Computer Usage

You are not limited to the use of a scientific calculator for homewwork problems. You may use a graphing calculator or computer to aid you in repetitive calculations or plotting functions for visualization.

```

## Exercise 1 
(P16.2 - modified)

````{exercise} 
:label: hw_bending_1

A 2000 mm long thin-walled cantilever beam with an unsymmetric cross-section supports two shear loads of 800 N and 400 N through the shear centre at its free end as shown below. Calculate the maximum normal stress due to bending that occurs at the fixed end of the beam and clearly indicate if it is tensile or compressive.

```{figure} ./Figures/hw_bending_1.svg
:alt: Unsymmetric cantilever beam with horizontal load of 400 N and vertical load of 800 N acting at its end
:width: 90%
:align: center
```
````

Here are some conceptual questions to test your understanding of the problem.

<iframe src="https://tudelft.h5p.com/content/1292900671403187657/embed" aria-label="Homework Quiz - Bending P1" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>

````{solution} hw_bending_1
:class: dropdown

::::{tab-set}
:::{tab-item} Final Answer

The maximum normal stress at the fixed end is:

$\sigma_A = 390~MPa$ (in tension)

and occurs at the free edge of the $1.0~mm$ thick flange of the beam cross-section.

:::
:::{tab-item} Intermediate Answers
**Centroid Location**: $50~mm$ above the lower flange and $13.3~mm$ to the right of the vertical web.

**Area Moments of Inertia**: $I_{xx} = 567 \times 10^3~mm^4$, $I_{yy} = 149 \times 10^3~mm^4$, $I_{xy} = -80 \times 10^3~mm^4$

**Moments at Fixed End**: $M_x = -1600~Nm$, $M_y = 800~Nm$

:::

::::
````

## Exercise 2 
(P16.4 - modified)
````{exercise} 
:label: hw_bending_2
Consider the thin-walled cantilever beam of constant thickness t with the cross-section shown below. The beam is subjected to a point force 2P in the negative x-direction at its mid-span and a point force of P in the negative y-direction at its free end. Both forces act at the shear centre (ie: they do not cause any torsion). Calculate the parametric expressions for the bending stresses at points 1 and 2 as a function of z.

```{figure} ./Figures/hw_bending_2.svg
:alt: Unsymmetric cantilever beam with horizontal load of 2P acting midspan and vertical load of P acting at its end. 
:width: 90%
:align: center
```
````

````{solution} hw_bending_2
:class: dropdown
::::{tab-set}
:::{tab-item} Final Answer

For $\left( 0 < z < \frac{L}{2} \right)$:

$\sigma_1 \left(z\right) = -\frac{0.1P}{ta^2}\left(L-z\right)$ and $\sigma_2 \left(z\right) = -\frac{1.26P}{ta^2}\left(L-z\right)$

For $\left( \frac{L}{2} < z < L \right)$:

$\sigma_1 \left(z\right) = \frac{P}{ta^2}\left(3.6z-1.85L\right)$ and $\sigma_2 \left(z\right) = \frac{P}{ta^2}\left(-1.46z + 0.1L\right)$

:::
:::{tab-item} Intermediate Answers
**Area Moments of Inertia**: $I_{xx} = \frac{2ta^3}{3}$, $I_{yy} = \frac{5ta^3}{12}$, $I_{xy} = \frac{ta^3}{4}$

**Internal Moments**: 

$M_x \left(z\right) = P\left(L-z\right)$ along the entire beam

$M_y \left(z\right) = 2P\left(\frac{L}{2}-z\right)$ from $\left( 0 < z < \frac{L}{2} \right)$ and 0 everywhere else

:::
::::
````

## Exercise 3
(P16.5)

````{exercise} 
:label: hw_bending_3
Consider the thin-walled z-stiffener profile cross-section shown below. Calculate and sketch the normal stress distribution in the cross-section for an internal bending moment $M_x$.

*Hint*: Since $\bar x$ is very small, you can assume it is zero with minimal error in your analysis (can you explain why?).

```{image} ./Figures/hw_bending_3.svg
:alt: unsymmetric z-stiffener profile. Top flange is width h/2 and thickness 2t. Lower flange is width h and thickness t. Vertical web is height 2t and width 2t. 
:width: 50%
:align: center
```
````

````{solution} hw_bending_3
:class: dropdown
::::{tab-set}
:::{tab-item} Final Answer

$\sigma  = \frac{{{M_x}}}{{{h^3}t}}\left( {0.91x + 0.50y} \right)$

```{image} ./Figures/hw_bending_3_sol.svg
:alt: normal stress distribution 
:width: 50%
:align: center
```

:::
:::{tab-item} Intermediate Answers

**Centroid Location**: midway between top and bottom flange and assumed to lay on the web (in reality it is $\frac{h}{24}$ to the right of the flange, but this assumption only creates a 2.6% error in $I_{yy}$)

**Area Moments of Inertia**: $I_{xx} = \frac{10h^3t}{3}$, $I_{yy} = \frac{5h^3t}{12}$, $I_{xy} = -\frac{3h^3t}{4}$

:::
::::
````

## Exercise 4
(P16.6 - modified)
````{exercise} 
:label: hw_bending_4
Consider the thin-walled z-stiffener cross-section shown below where the angle of the web is defined parametrically by angle $\theta$ with respect to the x-axis. For the given geometry and internal moment of $1.0~kNm$ shown below, calculate the location of the neutral axis ($\beta$) as functions of the web angle $\theta$. Then calculate the normal stresses at points 1, 2, 3 and 4 for angles $\theta = 30^\circ$, $60^\circ$, $90^\circ$, and $120^\circ$.

```{image} ./Figures/hw_bending_4.svg
:alt: z-stiffener profile with internal horizontal moment of 10kNm and parametric web angle theta
:width: 40%
:align: center
```
````

````{solution} hw_bending_4
:class: dropdown
::::{tab-set}
:::{tab-item} Final Answer

$\beta \left( \theta  \right) = {\tan ^{ - 1}}\left[ {\frac{{\frac{2}{3}\sin \theta \cos \theta }}{{\left( {\frac{1}{6} + 2{{\left( {\cos \theta  - \frac{1}{2}} \right)}^2} + \frac{2}{3}{{\cos }^2}\theta } \right)}}} \right]$

Click run to plot the location of the N.A. as a function of $\theta$
```{pyodide}
import matplotlib.pyplot as plt
import numpy as np

x_deg = np.linspace(0, 180, 500)

x_rad = np.radians(x_deg)

y = np.arctan(
    ((2/3) * np.sin(x_rad) * np.cos(x_rad)) /
    ((1/6) + 2*(np.cos(x_rad)-(1/2))**2 + (2/3) * np.cos(x_rad)**2)
)

y_deg = np.degrees(y)

plt.figure(figsize=(8, 3))
plt.plot(x_deg, y_deg)
plt.grid(True)

plt.xlabel('theta (degrees)')
plt.ylabel('beta (degrees)')
plt.show()
```

| $\theta$ [deg]    | $\sigma_1$ [MPa] |$\sigma_2$ [MPa] |$\sigma_3$ [MPa] |$\sigma_4$ [MPa] |
| -------- | ------- |------- |------- |------- |
| 30       | -174    | -74.6    | 74.6    | 173.6    |
| 60       | -137     | -45.8     | 45.8     | 137     |
| 90       | -69.4    | -69.4    | 69.4    | 69.4    |
| 120      | -64.2    | -75.8    | 75.8    | 64.2    |

:::
:::{tab-item} Intermediate Answers

**Centroid Location**: located in the centre of the web, no matter tha angle $\theta$

**Area Moments of Inertia**: 

$I_{xx}\left(\theta\right) = \frac{8t{a^3}}{3}{\sin ^2}\theta $, 

$I_{yy}\left(\theta\right) = t{a^3}\left[ {\frac{1}{6} + 2{{\left( {\cos \theta  - \frac{1}{2}} \right)}^2} + \frac{2}{3}{{\cos }^2}\theta } \right]$, 

$I_{xy}\left(\theta\right) = \frac{2}{3}t{a^3}\sin \theta \cos \theta $

**Internal Moments**: Due to direction of the internal moment, $M_x = -1~kNm$ and $M_y = 0$

:::
::::
````


## Exercise 5
(P16.8 - modified)
````{exercise} 
:label: hw_bending_5
Consider the thin-walled S-stiffener cross-section with a constant thickness $t$ and an internal moment of $30~Nm$ aligned with the centroidal y-axis shown below. Calculate the angle of the neutral axis, $\beta$, and the maximum normal stress due to bending if $r = 10~mm$ and $t = 0.8~mm$.

```{image} ./Figures/hw_bending_5.svg
:alt: S-stiffener profile with internal horizontal moment of 50Nm
:width: 50%
:align: center
```
````

````{solution} hw_bending_5
:class: dropdown
::::{tab-set}
:::{tab-item} Final Answer

$\beta = -67^\circ$

Points furthest from N.A. are points 1 and 3. This can be deduced from accurately drawing N.A. over the cross-section and identifying the points furthest from the N.A. or by taking the derivative of the normal stress equation and setting it to zero.

 Thus $\left| {{\sigma _{\max }}} \right| = \left| {{\sigma _1}} \right| = 220.5MPa$

:::
:::{tab-item} Intermediate Answers

**Centroid Location**: located at the point of inflection (point 2) by inspection

**Area Moments of Inertia**: 

$I_{xx} = 3 \pi t r^3 = 7.54 \times 10^3~mm^4$, 

$I_{yy} = \pi t r^3 = 2.51 \times 10^3~mm^4$, 

$I_{xy} = -4 t r^3 = -3.20 \times 10^3~mm^4$

**Internal Moments**: Due to direction of the internal moment, $M_x = 0$ and $M_y = -30~Nm$

**Normal Stress**: $\sigma \left( {x,y} \right) = \frac{{{M_y}}}{{{r^3}t}}\left( {0.693x + 0.294y} \right)$

:::
::::
````
