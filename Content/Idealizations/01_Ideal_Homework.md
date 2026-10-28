# Homework
These are the recommended homework problems for the topics of **Combined Open & Closed Sections** and **Structural Idealizations**. 

```{warning} Remember

You are not limited to the use of a scientific calculator for homework problems. You may use a graphing calculator or computer to aid you in repetitive calculations or plotting functions for visualization.

```


## Combined Open & Closed Sections

Note, the next three problems all use the same wingbox profile, so you only need to calculate section properties for it once.

### Exercise 1 (19.2)
````{exercise} 
:label: hw_combined_1

Consider the wing box section shown below consisting of two closed cells $1278$ and $3456$ connected by segment $23$ subjected to a $100~kN$ vertical shear force acting through the shear centre of the cross-section as shown below. All segments of the profile have a uniform thickness of $2.0~mm$. Calculate the shear stress at the mid-point of web $36$.

```{figure} ./Figures/hw_combined_1.svg
:alt: Thin-walled symmetric wingbox profile with a constant thickness. The profile is subjected to a vertical shear load of 100 kN acting through its shear centre.
:width: 90%
:align: center
```

````

````{solution} hw_combined_1
:class: dropdown
::::{tab-set}
:::{tab-item} Final Answer

The shear stress at the midpoint of web 34 is: $\tau = 48.2~MPa$

:::
:::{tab-item} Intermediate Answers

Location of the centroidal axis: $\tilde y = 168.4~mm$

Relevant section properties: ${I_{xx}} = 1.578 \times {10^8}~m{m^4}$

:::
::::
````

### Exercise 2 (19.3)
````{exercise} 
:label: hw_combined_2

Consider a new load case for the same wingbox profile as the previous problem. The load case is now an internal torque of $100~kNm$. Calculate the rate of twist and maximum shear stress in the wingbox. You can assume the wingbox is made of a single material with a shear modulus $G = 25000 N/mm^2$.

```{figure} ./Figures/hw_combined_2.svg
:alt: Thin-walled symmetric wingbox profile with a constant thickness. The profile is subjected to an internal torque of 100 kNm.
:width: 90%
:align: center
```
````
````{solution} hw_combined_2
:class: dropdown
::::{tab-set}
:::{tab-item} Final Answer

Rate of twist: $\frac{d\theta}{dz}=1.85 \times 10^{-5}~rad/mm$

Maximum shear stress: $\tau_{max} = 85.05~MPa$

:::
:::{tab-item} Intermediate Answers

Relevant section properties: ${I_{xx}} = 1.578 \times {10^8}~m{m^4}$

:::
::::
````

### Exercise 3 (19.4)
````{exercise} 
:label: hw_combined_3

Consider a new load case for the same wingbox profile as the previous two problem. The load case is now an internal vertical shear force of $100~kN$ aligned with web $72$ of the wingbox. Calculate the rate of twist and maximum shear stress in the wingbox. You can assume the wingbox is made of a single material with a shear modulus $G = 25000 N/mm^2$.

```{figure} ./Figures/hw_combined_3.svg
:alt: Thin-walled symmetric wingbox profile with a constant thickness. The profile is subjected to an internal shear force of 100 kN aligned with web 72 of the section.
:width: 90%
:align: center
```
````
````{solution} hw_combined_3
:class: dropdown
::::{tab-set}
:::{tab-item} Final Answer

Rate of twist: $\frac{d\theta}{dz}=5.6 \times 10^{-6}~rad/mm$

Maximum shear stress: $\tau_{max} = 74.0~MPa$

:::
:::{tab-item} Intermediate Answers

Relevant section properties: ${I_{xx}} = 1.578 \times {10^8}~m{m^4}$

:::
::::
````

### Exercise 4 (19.5)
````{exercise} 
:label: hw_combined_4

You are now asked to analyze a new wingbox profile shown below. The wingbox has a thickness of $2.0~mm$ everywhere except the vertical web $36$ which has a thickness of $4.0~mm$. Calculate the rate of twist and maximum shear stress in the wingbox for an internal vertical shear force of $50~kN$ aligned with web $36$. You can assume the wingbox is made of a single material with a shear modulus $G = 25000 N/mm^2$.

```{figure} ./Figures/hw_combined_4.svg
:alt: Thin-walled symmetric wingbox profile with a variable thickness. The profile is subjected to an internal shear force of 50 kN aligned with web 36 of the section.
:width: 80%
:align: center
```
````
````{solution} hw_combined_4
:class: dropdown
::::{tab-set}
:::{tab-item} Final Answer

Rate of twist: $\frac{d\theta}{dz}=3.23 \times 10^{-4}~rad/mm$

Maximum shear stress: $\tau_{max} = 441.3~MPa$

:::
:::{tab-item} Intermediate Answers

Relevant section properties: ${I_{xx}} = 8.8 \times {10^5}~m{m^4}$

:::
::::
````
## Structural Idealizations

### Exercises 5 (20.2)
````{exercise} 
:label: hw_ideal_1
Given below is an idealized wingbox consisting of eight booms connected by zero-thickness shear carrying webs. Booms 1, 4, 5, and 8 have an area of $200~mm^2$ while the reaming booms have an area of $250~mm^2$. Considering an internal vertical shear force of $1495~N$ due to lift acting through the shear centre of the section, calculate the shear flow distribution within the wingbox and the location of the shear centre.

```{figure} ./Figures/hw_ideal_1.svg
:alt: Idealized wingbox profile with a 8 booms and one vertical web. 
:width: 90%
:align: center
```

````

````{solution} hw_ideal_1
:class: dropdown
::::{tab-set}
:::{tab-item} Final Answer

**Location of the Shear Centre**

```{figure} ./Figures/hw_ideal_1_sc.svg
:alt: Illustration of the location of the shear centre for Exercise 5. 
:width: 80%
:align: center
```
**Shear Flow Distribution**

```{figure} ./Figures/hw_ideal_1_sf.svg
:alt: Illustration of the shear flow distribution for Exercise 5. 
:width: 80%
:align: center
```

:::
:::{tab-item} Intermediate Answers

Relevant section properties: ${I_{xx}} = 8.04 \times {10^6}~m{m^4}$

:::
::::
````

### Exercise 6
````{exercise} 
:label: hw_ideal_6
Consider the polygonal wingbox section shown below left subjected to an internal Torque $T = 9~kNm$, an internal vertical shear force $V = 100~kN$ aligned with the $y$-axis, and an internal bending moment $M = 20~kNm$ aligned with the $x$-axis. You are tasked with analyzing this section by doing the following:
- Idealize the section as illustrated below right by calculating the appropriate boom areas for each of the 6 booms;
- Calculate the maximum internal normal stress in the cross-section using your idealization
- Calculate the magnitude of the maximum internal shear stress in the cross-section using your idealization

```{figure} ./Figures/hw_ideal_2.svg
:alt: Hexaganol wingbox profile with a suggested 6 boom idealization. 
:width: 100%
:align: center
```

````

````{solution} hw_ideal_6
:class: dropdown
::::{tab-set}
:::{tab-item} Final Answer

**Boom Areas**

$B_1 = B_3 = B_4 = B_6 = 244~mm^2$

$B_2 = B_5 = 264~mm^2$

**Maximum Shear Stress**

$\tau_{max} = 214.5~MPa$ and occurs in wall $34$

**Maximum Normal Stress**

$|\sigma_{max}| = 259~MPa$ and occurs at booms $2$ and $5$

:::
:::{tab-item} Intermediate Answers

Relevant section properties: ${I_{xx}} = 7.72 \times {10^6}~m{m^4}$

:::
::::
````



### Exercise 7
````{exercise} 
:label: hw_ideal_7

You are tasked with analyzing a section of the rear fuselage structure for a horizontal gust load acting on the vertical stabilizer. Your fellow engineer has already idealized the fuselage section and determined the internal loading at this location, providing you with the information below. Given this idealization:
- Calculate the shear flows acting in the idealized fuselage section
- Calculate the location of the neutral axis and the **maximum compressive normal stress** acting in the idealized section

```{figure} ./Figures/hw_ideal_3.svg
:alt: Idealize circular fuselage section consisting of 4 booms and subjected to an internal bending moment and offset horizontal gust load. 
:width: 80%
:align: center
```

````

````{solution} hw_ideal_7
:class: dropdown
::::{tab-set}
:::{tab-item} Final Answer

**Shear Flow Distribution**

```{figure} ./Figures/hw_ideal_3_sf.svg
:alt: Idealize circular fuselage section consisting of 4 booms and subjected to an internal bending moment and offset horizontal gust load with final shear flow distribution overlaid on section. 
:width: 70%
:align: center
```

**N.A. location and Maximum Compressive Normal Stress**

```{figure} ./Figures/hw_ideal_3_na.svg
:alt: Idealize circular fuselage section consisting of 4 booms and subjected to an internal bending moment and offset horizontal gust load with neutral axis location and maximum compressive bending stress overlaid.
:width: 70%
:align: center
```

:::
:::{tab-item} Intermediate Answers

Relevant section properties: 

${I_{xx}} = 1.89 \times {10^8}~m{m^4}$

${I_{yy}} = 1.17 \times {10^8}~m{m^4}$

:::
::::
````



### Exercise 8
````{exercise} 
:label: hw_ideal_8

You are tasked with analyzing the transverse shear loading of a cubesat main body. A schematic of the real section of the satellite is shown below left. It contains a stiffening element of area $A = 20~mm^2$ at each of the corners of the section, and thin-walled panels with thicknesses of either $0.6~mm$ or $1.4~mm$ according to the diagram below. The cross-section is symmetric about the x-axis, but not about the y-axis.The load case to be analyzed is an internal shear force $V = 2.0~kN$ acting through the midpoint of sidewall 12.

```{figure} ./Figures/hw_ideal_4.svg
:alt: Rectangular satellite bus cross-section with corner stiffeners and suggested idealization. 
:width: 90%
:align: center
```
Using the suggested idealization shown above right, complete the following:
- Calculate the areas of the four booms for the internal load case provided
- Calculate the magnitude and location of the maximum shear stress in the cross-section.


````

````{solution} hw_ideal_8
:class: dropdown
::::{tab-set}
:::{tab-item} Final Answer

**Boom Areas**

$B_1 = B_4 = 60.0~mm^2$

$B_2 = B_3 = 73.3~mm^2$

**Maximum Shear Stress**

**NOTE:** the maximum shear stress **is not** located where the maximum shear flow is!

$\tau_{max} = 15.8~MPa$ and occurs in wall $14$. 

:::
:::{tab-item} Intermediate Answers

Relevant section properties: 

${I_{xx}} = 6.67 \times {10^5}~m{m^4}$

:::
::::
````