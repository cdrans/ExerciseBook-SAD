# Homework

These are the recommended homework problems for the topic of Bending.

```{warning} Remember

You are not limited to the use of a scientific calculator for homewwork problems. You may use a graphing calculator or computer to aid you in repetitive calculations or plotting functions for visualization.

```

## P16.2 (modified)

````{exercise} 1
:label: hw_bending_1

A 2000 mm long thin-walled cantilever beam with an unsymmetric cross-section supports two shear loads of 800 N and 400 N through the shear centre at its free end as shown below. Calculate the maximum normal stress due to bending that occurs at the fixed end of the beam and clearly indicate if it is tensile or compressive.

```{figure} /Content/Bending/Figures/P16-2.svg
:alt: Unsymmetric cantilever beam with horizontal load of 400 N and vertical load of 800 N acting at its end
:width: 600px
:align: center
```
````


````{solution} hw_bending_1
:class: dropdown

::::{tab-set}
:::{tab-item} Final Answer Check

The maximum normal stress at the fixed end is: $\sigma_{max} = 390~MPa$ (in tension)

:::
:::{tab-item} Interpret
In order to determine the maximum bending stress, we need to:
- Identify the internal loading at the fixed end
- Identify the location of the maximum bending stress in the cross-section (point furthest from the N.A.)

To accomplish this, we need to establish a centroidal coordinate frame for our analysis and references for locating the centroid and N.A.

```{figure} /Content/Bending/Figures/16-2_I_1.svg
:alt: Coordinate frame and references needed to solve the problem 
:width: 80%
:align: center
```

:::
:::{tab-item} Develop
**Bending Stress Equation**
Apply the generalized bending stress equation:
$${\sigma _z} = \frac{{\left( {{M_x}{I_{yy}} - {M_y}{I_{xy}}} \right)y + \left( {{M_y}{I_{xx}} - {M_x}{I_{xy}}} \right)x}}{{{I_{xx}}{I_{yy}} - I_{xy}^2}}$$

All terms are none-zero in this problem, so it does not simplify further here.

**Locate N.A. to identify location of max stress**
Location of the N.A. is determined by setting the above equation to zero (as N.A. is defined as line where $\sigma_z = 0$). This results in:
$$\frac{y}{x} =  - \frac{{{M_y}{I_{xx}} - {M_x}{I_{xy}}}}{{{M_x}{I_{yy}} - {M_y}{I_{xy}}}}$$

For our definition of $\theta$, $\frac{y}{x} = tan \theta$, thus:
$$\theta  = {\tan ^{ - 1}}\left( { - \frac{{{M_y}{I_{xx}} - {M_x}{I_{xy}}}}{{{M_x}{I_{yy}} - {M_y}{I_{xy}}}}} \right)$$

**Locate Centroid**
As area of the upper and lower flange are the same, using thin-walled approximations we can deduce that $\bar y = 50~mm$, while:

$$\bar x = \sum {\frac{{{A_i} \cdot {{\tilde x}_i}}}{{{A_i}}}} $$

**Internal Moments**
Each shear force at the free end creates a moment equal to the shear force times the length of the beam. Need to apply the correct sign to these moments for the defined coodinate frame.

**Area Moments of Inertia** 
Calculate the relevant area moments of inertia:
$${I_{xx}} = \int\limits_A {{y^2}dA = \sum {\left( {{{\bar I}_{xx}} + A \cdot {y^2}} \right)} } $$
$${I_{yy}} = \int\limits_A {{x^2}dA = \sum {\left( {{{\bar I}_{yy}} + A \cdot {x^2}} \right)} } $$
$${I_{xy}} = \int\limits_A {xydA = \sum {\left( {{{\bar I}_{xy}} + A \cdot xy} \right)} } $$



:::
:::{tab-item} Evaluate

**Internal Moments**: At the fixed end,  $M_x = -1600~Nm$ and $M_y = 800~Nm$

**Locate Centroid**: $\bar x = 13.3~mm$ and $\bar y = 50~mm$

**Area Moments of Inertia**: $I_{xx} = 567 \times 10^3~mm^4$, $I_{yy} = 149 \times 10^3~mm^4$, $I_{xy} = -80 \times 10^3~mm^4$

**Bending Stress Equation**
$${\sigma _z} = \left( {4.16\frac{{MPa}}{{mm}}} \right)x - \left( {2.24\frac{{MPa}}{{mm}}} \right)y$$

**Neutral Axis Location**: $\theta = 61.7^\circ$

**Max Stress**: With the N.A. located $61.7^\circ$ from the x-axis, then clearly the right-most point on the lower flange is furthest from the neutral axis. This point has the coordinates $x = 66.7~mm$ and $y = -50~mm$. Subbing these coordinates into the above bending stress equation, we get: $\sigma_{max} = 390~MPa$ (in tension)

:::
:::{tab-item} Assess

Looking at the loads applied to the end of the beam individually, each shear force would tend to create a tensile stress at the right-most point of the lower flange. Thus the fact that the maximum stress is tensile makes sense. 

:::

::::
````



```{seealso} Answer
:class: dropdown

The maximum normal stress at the fixed end is:

$\sigma_A = 390~MPa$ (in tension)

and occurs at the free edge of the $1.0~mm$ thick flange of the beam cross-section.
```

```{tip} Intermediate Answers
:class: dropdown

**Centroid Location**: $50~mm$ above the lower flange and $13.3~mm$ to the right of the vertical web.

**Area Moments of Inertia**: $I_{xx} = 567 \times 10^3~mm^4$, $I_{yy} = 149 \times 10^3~mm^4$, $I_{xy} = -80 \times 10^3~mm^4$

**Moments at Fixed End**: $M_x = -1600~Nm$, $M_y = 800~Nm$
```

### Test your understanding

Here are some conceptual questions to test your understanding of the problem.

<iframe src="https://tudelft.h5p.com/content/1292900671403187657/embed" aria-label="Homework Quiz - Bending P1" width="1088" height="637" frameborder="0" allowfullscreen="allowfullscreen" allow="autoplay *; geolocation *; microphone *; camera *; midi *; encrypted-media *"></iframe><script src="https://tudelft.h5p.com/js/h5p-resizer.js" charset="UTF-8"></script>

## P16.4

Consider the thin-walled cantilever beam of constant thickness t with the cross-section shown below. The beam is subjected to a point force 2P in the negative x-direction at its mid-span and a point force of P in the negative y-direction at its free end. Both forces act at the shear centre (ie: they do not cause any torsion). Calculate the parametric expressions for the bending stresses at points 1 and 2 as a function of z.

```{figure} /Content/Bending/Figures/P16-4.svg
:alt: Unsymmetric cantilever beam with horizontal load of 2P acting midspan and vertical load of P acting at its end. 
:width: 600px
:align: center
```

```{seealso} Answer
:class: dropdown

For $\left( 0 < z < \frac{L}{2} \right)$:

$\sigma_1 \left(z\right) = -\frac{0.1P}{td^2}\left(L-z\right)$ and $\sigma_2 \left(z\right) = -\frac{1.26P}{td^2}\left(L-z\right)$

For $\left( \frac{L}{2} < z < L \right)$:

$\sigma_1 \left(z\right) = \frac{P}{td^2}\left(3.6z-1.85L\right)$ and $\sigma_2 \left(z\right) = \frac{P}{td^2}\left(-1.46z + 0.1L\right)$
```

```{tip} Intermediate Answers
:class: dropdown

**Area Moments of Inertia**: $I_{xx} = \frac{2td^3}{3}$, $I_{yy} = \frac{5td^3}{12}$, $I_{xy} = \frac{td^3}{4}$

**Internal Moments**: 

$M_x \left(z\right) = P\left(L-z\right)$ along the entire beam

$M_y \left(z\right) = 2P\left(\frac{L}{2}-z\right)$ from $\left( 0 < z < \frac{L}{2} \right)$ and 0 everywhere else
```

## P16.5

Consider the thin-walled z-stiffener profile cross-section shown below. Calculate and sketch the normal stress distribution in the cross-section for an internal bending moment $M_x$.

*Hint*: Since $\bar x$ is very small, you can assume it is zero with minimal error in your analysis (can you explain why?).

```{image} /Content/Bending/Figures/P16-5.svg
:alt: unsymmetric z-stiffener profile. Top flange is width h/2 and thickness 2t. Lower flange is width h and thickness t. Vertical web is height 2t and width 2t. 
:width: 300px
:align: center
```

```{seealso} Answer
:class: dropdown

$\sigma  = \frac{{{M_x}}}{{{h^3}t}}\left( {0.91x + 0.50y} \right)$

![normal stress distribution](/Content/Bending/Figures/P16-5_sol.svg)
```

```{tip} Intermediate Answers
:class: dropdown

**Centroid Location**: midway between top and bottom flange and assumed to lay on the web (in reality it is $\frac{h}{24}$ to the right of the flange, but this assumption only creates a 2.6% error in $I_{yy}$)

**Area Moments of Inertia**: $I_{xx} = \frac{10h^3t}{3}$, $I_{yy} = \frac{5h^3t}{12}$, $I_{xy} = -\frac{3h^3t}{4}$

```

## P16.6 (modified)

Consider the thin-walled z-stiffener cross-section shown below where the angle of the web is defined parametrically by angle $\theta$ with respect to the x-axis. For the given geometry and internal moment of $1.0~kNm$ shown below, calculate the location of the neutral axis ($\beta$) as functions of the web angle $\theta$. Then calculate the normal stresses at points 1, 2, 3 and 4 for angles $\theta = 30^\circ$, $60^\circ$, $90^\circ$, and $120^\circ$.

```{image} /Content/Bending/Figures/P16-6.svg
:alt: z-stiffener profile with internal horizontal moment of 10kNm and parametric web angle theta
:width: 250px
:align: center
```

```{seealso} Answer
:class: dropdown

$\beta \left( \theta  \right) = {\tan ^{ - 1}}\left[ {\frac{{\frac{2}{3}\sin \theta \cos \theta }}{{\left( {\frac{1}{6} + 2{{\left( {\cos \theta  - \frac{1}{2}} \right)}^2} + \frac{2}{3}{{\cos }^2}\theta } \right)}}} \right]$

| $\theta$ [deg]    | $\sigma_1$ [MPa] |$\sigma_2$ [MPa] |$\sigma_3$ [MPa] |$\sigma_4$ [MPa] |
| -------- | ------- |------- |------- |------- |
| 30       | -174    | -74.6    | 74.6    | 173.6    |
| 60       | -137     | -45.8     | 45.8     | 137     |
| 90       | -69.4    | -69.4    | 69.4    | 69.4    |
| 120      | -64.2    | -75.8    | 75.8    | 64.2    |

```{image} /Content/Bending/Figures/P16-6_sol.png
:alt: neutral axis location plot
:width: 500px
:align: center

```

```{tip} Intermediate Answers
:class: dropdown

**Centroid Location**: located in the centre of the web, no matter tha angle $\theta$

**Area Moments of Inertia**: 

$I_{xx}\left(\theta\right) = \frac{8t{a^3}}{3}{\sin ^2}\theta $, 

$I_{yy}\left(\theta\right) = t{a^3}\left[ {\frac{1}{6} + 2{{\left( {\cos \theta  - \frac{1}{2}} \right)}^2} + \frac{2}{3}{{\cos }^2}\theta } \right]$, 

$I_{xy}\left(\theta\right) = \frac{2}{3}t{a^3}\sin \theta \cos \theta $

**Internal Moments**: Due to direction of the internal moment, $M_x = -1~kNm$ and $M_y = 0$

```

## P16.8 (modified)

Consider the thin-walled S-stiffener cross-section with a constant thickness $t$ and an internal moment of $30~Nm$ aligned with the centroidal y-axis shown below. Calculate the angle of the neutral axis, $\beta$, and the maximum normal stress due to bending if $r = 10~mm$ and $t = 0.8~mm$.

```{image} /Content/Bending/Figures/P16-8.svg
:alt: S-stiffener profile with internal horizontal moment of 50Nm
:width: 300px
:align: center
```

```{seealso} Answer
:class: dropdown

$\beta = -67^\circ$

Points furthest from N.A. are points 1 and 3. This can be deduced from accurately drawing N.A. over the cross-section and identifying the points furthest from the N.A. or by taking the derivative of the normal stress equation and setting it to zero.

 Thus $\left| {{\sigma _{\max }}} \right| = \left| {{\sigma _1}} \right| = 220.5MPa$

```

```{tip} Intermediate Answers
:class: dropdown

**Centroid Location**: located at the point of inflection (point 2) by inspection

**Area Moments of Inertia**: 

$I_{xx} = 3 \pi t r^3 = 7.54 \times 10^3~mm^4$, 

$I_{yy} = \pi t r^3 = 2.51 \times 10^3~mm^4$, 

$I_{xy} = -4 t r^3 = -3.20 \times 10^3~mm^4$

**Internal Moments**: Due to direction of the internal moment, $M_x = 0$ and $M_y = -30~Nm$

**Normal Stress**: $\sigma \left( {x,y} \right) = \frac{{{M_y}}}{{{r^3}t}}\left( {0.693x + 0.294y} \right)$


```
