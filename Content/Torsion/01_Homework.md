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

**Maximum Shear Stress**: $\tau_{max} = 83.3MPa$ 

**Rate of Twist**: 

|  distance from fixed end [mm]    | $d \theta$ [deg/m] |
| -------- | ------- |
| 0       | 1.343   | 
| 1000       | 1.480    | 
| 2000     | 1.647    | 
| 3000     | 1.857   | 

**Estimated Angle of Twist**: $\theta \approx 4.74^\circ$ 

:::
:::{tab-item} Intermediate Answers

Etablish coordinate frame. For this solution, z is the position along the legnth of the beam where $z = 0$ corresponds to the fixed end.

$h\left( z \right) = 400\left[ {mm} \right] - 0.033z$

$ A_m \left( z \right) = 4 \times {10^4}\left[ {m{m^2}} \right] - 3.33\left[ {mm} \right] \cdot z$

**How to Estimate Angle of Twist**: 

We can estimate the angle of twist using the intervals of rate of twist by applying the trapazoidal rule, since the angle of twist would be the integral of rate of twist along the length of the beam, and thus the area under the rate of twist vs position along beam graph.

If the angle of twist is calculated by integration rather than estimation, then you get $\theta = 4.718^\circ$

:::
::::
````

## Exercise 4


````{exercise} 
:label: hw_torsion_4

Consider a thin-walled aluminum beam ($G = 30~GPa$) with the cross-section shown below. All of the dimensions of the cross-section are set below, except for the constant thickness, $t$, which you need to determine based on the below design requirements. Determine the appropriate thickness that meets the foloowing requirements:
1. Section must withstand an internal torque of $80~Nm$
2. Maximum allowable shear stress: $\tau_{max} = 175~MPa$
3. Maximum rate of twist: $\left( \frac{d\theta}{dz} \right)_{max} = 1~\frac{rad}{m}$
4. Thickness must be specified in tenths of a millimeter    
5. Weight must be minimized


```{figure} ./Figures/hw_torsion_4.svg
:alt: Thin=walled beam cross-section with a constant thickness t
:width: 60%
:align: center
```
````

````{solution} hw_torsion_4
:class: dropdown
::::{tab-set}
:::{tab-item} Final Answer
The thickness of the section that meets all of the design requirements is: 

$t = 3.4~mm$

:::
:::{tab-item} Intermediate Answers

Minimum thickness for requirement 2: $t_{min} = 2.593~mm$

Minimum thickness for requirement 3: $t_{min} = 3.397~mm$

Based on above, and considering requirement 4 and 5, the minimum thickness would be:

$t_{min} = 3.4~mm$

At this thickness: $\tau_{max} = 102~MPa$ and $\frac{d\theta}{dz} = 0.998~\frac{rad}{m}$

:::
::::
````

## Exercise 5


````{exercise} 
:label: hw_torsion_5

Consider a thin-walled beam with the parametric cross-section shown below. Calculate the parametric magnitudes of the maximum shear stress and the rate of twist of the beam for an internal torque $T$. You can assume the beam is made of a single material with shear modulus $G$ for your calculations. 

```{figure} ./Figures/hw_torsion_5.svg
:alt: Thin-walled beam cross-section with regions of thickness of 2t and t.
:width: 50%
:align: center
```
````


````{solution} hw_torsion_5
:class: dropdown
::::{tab-set}
:::{tab-item} Final Answer

$\tau_{max} = \frac{0.284T}{rt^2}$ (occurs in thicker portions of the beam)

$\frac{d\theta}{dz} = \frac{0.142T}{rt^3}$

:::
:::{tab-item} Intermediate Answers

From compatability: $T_{12} = T_{67} = 1.556T_{26}$

From superposition: $T = 2T_{12} + T_{26}$

:::
::::
````

## Exercise 6a


````{exercise} 
:label: hw_torsion_6a

Consider a thin-walled wing box structure comprised of a semi-circular leading edge of radius $r = 50~mm$ joined to square of width $100~mm$ as illustrated below. The wing box is made of aluminum ($G = 25~GPa$) with a constant thickness, $t = 2~mm$, and is subjected to a uniform distributed torque of $500 Nm/m$.

```{figure} ./Figures/hw_torsion_6a.svg
:alt: Thin-walled closed beam section with uniform distributed torsion applied along its length.
:width: 80%
:align: center
```

Calculate the angle of twist of the wing box ($\theta_B$) with respect to the fixed end $A$ **AND** the maximum **shear stress** in the wing box due to the uniform distributed torque. 

````

````{solution} hw_torsion_6a
:class: dropdown
::::{tab-set}
:::{tab-item} Final Answer

$\theta_B/A} =  -2.71^\circ $

$\left| {{\tau _{\max }}} \right| = 36.0~MPa$

:::
:::{tab-item} Intermediate Answers

$A_m = 0.014~m^2$

$T\left( z \right) = \left( 500~\frac{Nm}{m}\right) \left{ L-z \right)$

:::
::::
````

## Exercise 6b


````{exercise} 
:label: hw_torsion_6b

A design modification to the wing box from {numref}`hw_torsion_6a` results in a $0.2~m$ length of the upper skin being removed between points $C$ and $D$ as illustrated below.

```{figure} ./Figures/hw_torsion_6b.svg
:alt: Thin-walled beam section with uniform distributed torsion applied along its length. The section is closed from the root to point C and open from C to the tip.
:width: 100%
:align: center
```
Calculate the new angle of twist of the modified wing box ($\theta_B$) with respect to the fixed end $A$ **AND** the maximum **shear stress** in the modified wing box due to the uniform distributed torque.

````

````{solution} hw_torsion_6b
:class: dropdown
::::{tab-set}
:::{tab-item} Final Answer

$\theta_B/A} =  -26.8^\circ $

$\left| {{\tau _{\max }}} \right| = 210~MPa$

:::
:::{tab-item} Intermediate Answers

$A_m = 0.014~m^2$

$T\left( z \right) = \left( 500~\frac{Nm}{m}\right) \left{ L-z \right)$

$\theta_C/A} =  -2.70^\circ $

$\theta_B/C} =  -24.07^\circ $

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


