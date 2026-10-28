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

### Exercises
````{exercise} 
:label: hw_ideal_99
text
````

````{solution} hw_ideal_99
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



