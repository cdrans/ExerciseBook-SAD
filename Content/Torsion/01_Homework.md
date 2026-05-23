# Homework
These are the recommended homework problems for the topic of Torsion. 

```{warning} Remember

You are not limited to the use of a scientific calculator for homework problems. You may use a graphing calculator or computer to aid you in repetitive calculations or plotting functions for visualization.

```


## Exercise 1
(18.1 modified)

Consider the uniform, multi-material, thin-walled, cantilever beam with a closed rectangular cross-section shown below. The upper and lower flanges are made out of $1.2~mm$ thick aluminum alloy with a shear modulus of $G_1 = 25~GPa$ while the two vertical webs are made of a titanium alloy with a thickness of $1.8~mm$ and shear modulus $G_2 = 45~GPa$. The beam is subjected to a uniform distributed torque of $30~Nm/mm$ along its length as well as a point torque of $20~kNm$ applied at the free end of the beam in the opposite direction of the distributed torque. 

Calculate the following:
- magnitude and location of the maximum shear stress in the beam
- the distribution of angle of twist along the length of the beam

````{exercise} 
:label: hw_torsion_1

```{figure} ./Figures/P18-1_modified.svg
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






