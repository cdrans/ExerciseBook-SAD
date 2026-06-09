# Homework
These are the recommended homework problems for the topic of Torsion. 

```{warning} Remember

You are not limited to the use of a scientific calculator for homework problems. You may use a graphing calculator or computer to aid you in repetitive calculations or plotting functions for visualization.

```


## Exercise 1
(18.1 modified)

````{exercise} 
:label: hw_torsion_1

Consider the $3000~mm$ long uniform, multi-material, thin-walled, cantilever beam with a closed rectangular cross-section shown below. The upper and lower flanges are made out of $1.2~mm$ thick aluminum alloy with a shear modulus of $G_1 = 25~GPa$ while the two vertical webs are made of a titanium alloy with a thickness of $1.8~mm$ and shear modulus $G_2 = 45~GPa$. The beam is subjected to a uniform distributed torque of $30~Nm/mm$ along its length as well as a point torque of $20~kNm$ applied at the free end of the beam in the opposite direction of the distributed torque. 

Calculate the following:
- magnitude and location of the maximum shear stress in the beam
- the distribution of angle of twist along the length of the beam

```{figure} ./Figures/hw_torsion_1.svg
:alt: Multi-material thin-walled rectangular cantilever beam with a distributed torque of 30Nm/mm and a point torque of 20kNm in the opposite direction of the distributed torque applied at the free end of the beam.
:width: 100%
:align: center
```
````

````{solution} hw_torsion_1
:class: dropdown
::::{tab-set}
:::{tab-item} Final Answer

**Max shear stress:** Occurs at the fixed end of the beam in the aluminum flanges.

$\tau_{max} = 159~MPa$

**Distribution of angle of twist:**

$\theta \left( z \right) = 2.816 \times {10^{ - 5}}\left[ {\frac{{rad}}{{mm}}} \right] \cdot z - 6.033 \times {10^{ - 9}}\left[ {\frac{{rad}}{{m{m^2}}}} \right] \cdot {z^2}$

```{pyodide}
import matplotlib.pyplot as plt
import numpy as np

## Range of z along the beam
z_mm = np.linspace(0, 3000, 500)

## Calculate angle of twist in radians
theta_rad = 2.816E-5 * z_mm - 6.033E-9 * z_mm**2

## Convert angle of twist to degrees
theta_deg = np.degrees(theta_rad)

plt.figure(figsize=(8, 3))
plt.plot(z_mm, theta_deg)
plt.grid(True)

plt.xlabel('z (mm)')
plt.ylabel('theta (degrees)')
plt.show()
```

:::
:::{tab-item} Intermediate Answers

**Internal Torque** 

$T\left( z \right) =  - 20\left[ {kNm} \right] + 30\left[ {Nm/mm} \right]\left( {3000mm - z} \right)$

**Rate of Twist**: 

$\frac{{d\theta }}{{dz}}\left( z \right) =  - 8.044 \times {10^{ - 6}}\left[ {\frac{{rad}}{{mm}}} \right] + 1.207 \times {10^{ - 8}}\left[ {\frac{{rad}}{{m{m^2}}}} \right] \cdot \left( {3000mm - z} \right)$

:::
::::
````

## Exercise 2

````{exercise} 
:label: hw_torsion_2

Consider the $2000~mm$ long uniform, thin-walled, beam with a closed circular cross-section. The beam is made of a metal alloy with a shear modulus $G = 30~GPa$ and has a constant wall-thickness of $2.5~mm$. The FBD of the beam below shows the applied loading consisting of a distributed torque of $1.0~Nm/mm$ and two point end torques of $450~Nm$ all acting in the same direction. This loading is reacted by two moment couples, $T$, acting $500~mm$ from each end of the beam. 

Calculate the following:
- magnitude of $T$ required to keep the beam in static equilibrium
- magnitude and location of the maximum shear stress in the beam
- the distribution of angle of twist along the length of the beam (use the centre of the beam, $z = 0$, as your datum for expressing the angle of twist of the beam)

```{figure} ./Figures/hw_torsion_2.svg
:alt: Torsional shaft with symmetric loading across the midpoint of the shaft. Subjected to a uniform distributed torque and 4 point torques.
:width: 100%
:align: center
```
````
 
````{solution} hw_torsion_2
:class: dropdown
::::{tab-set}
:::{tab-item} Final Answer

$T_o = 1450~Nm$

$\tau_{max} = 24.2~MPa$ at $z = \pm 500~mm$

**Angle of Twist**

For $\left( 0 < z < 500~mm \right)$:

$\theta \left( z \right) =  - \frac{w}{{4\pi {r^3} \cdot G \cdot t}}{z^2} = - 0.85 \times {10^{ - 9}}\left[ {\frac{{rad}}{{m{m^2}}}} \right] \cdot {z^2}$

For $\left( 500~mm < z < 1000~mm \right)$:

$\theta \left( z \right) = \frac{1}{{2\pi {r^3} \cdot G \cdot t}}\left( {{T_0}z - w\frac{{{z^2}}}{2}} \right) - 12.33 \times {10^{ - 3}}\left[ {rad} \right] = 1.70 \times {10^{ - 8}}\left( {1450z - \frac{{{z^2}}}{2}} \right)\left[ {\frac{{rad}}{{m{m^2}}}} \right] - 12.33 \times {10^{ - 3}}\left[ {rad} \right]$

:::
:::{tab-item} Intermediate Answers

Note, the internal loading at $z = 0$ is $0~Nm$ and the internal loading is symmetric across the datum

**Internal Loading**

For $\left( 0 < z < 500~mm \right)$:

$T \left( z \right) =  -wz$

For $\left( 500~mm < z < 1000~mm \right)$:

$T \left( z \right) = 1450~Nm - wz$


:::
::::
````

## Exercise 3


````{exercise} 
:label: hw_torsion_3

Consider the tapered thin-walled cantilever beam with a closed rectangular cross-section shown below. The beam has a constant width of $100~mm$; constant thickness, $t = 1.0~mm$; and varies in height from $300~mm$ at its free end to $400~mm$ at its fixed end. The beam is made of a metal alloy with a shear modulus $G = 25~GPa$ and is subjected to $5~kNm$ torque at its free end. Calculate the following:
- maximum shear stress in the beam 
- rate of twist along the beam at 1000 mm intervals along the beam
- angle of twist of the free end of the beam, approximated using the previously calculated rates of twist

```{figure} ./Figures/hw_torsion_3.svg
:alt: Tapered thin-walled canteliever beam with constant width and thickness subjected to a 5kNm torque at its free end.
:width: 80%
:align: center
```

````

````{solution} hw_torsion_3
:class: dropdown
::::{tab-set}
:::{tab-item} Final Answer

text

:::
:::{tab-item} Intermediate Answers

text

:::
::::
````





## Exercise 99


````{exercise} 
:label: hw_torsion_99

text

````

````{solution} hw_torsion_99
:class: dropdown
::::{tab-set}
:::{tab-item} Final Answer

text

:::
:::{tab-item} Intermediate Answers

text

:::
::::
````


