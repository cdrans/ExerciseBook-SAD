# Homework 

These are sample exam-level problems for the topic of Bending. We highly recommentd you follow the IDEA framework (see {numref}`fig_IDEA`) for approaching the solution of each problem. Write out your steps in this approach such that you can easily show a colleague and they could check your work. Effective communication of your solution is arguabbly more valaubale then getting the correct answer!

```{important} Designed for scientific calculators!

These exam problems are designed to be solved with only a basic scientific calculator. It is reccomended that you limit yourself to the bachelor TI-30xb calculator to match the calculator restrictions of the exam when solving these questions.

```

## Sample Exam Question 1

````{exercise} 
:label: exam_bending_1

Consider the variable thickness stringer profile shown below subjected to a bending moment $M$ aligned with the horizontal axis of the page. The stringer section can be assumed to be thin-walled $\left( t << L \right)$. The location of the centroid of the section is known and indicated in the figure. Answer the following bending related questions in relation to this cross-section, showing all relevant work needed to justify your answer.

```{figure} ./Figures/exam_bending_1.svg
:alt: Unsymmetric J-stiffener profile with internal moment M acting on it.
:width: 60%
:align: center
```
````

1. A fellow engineer has partially completed the analysis of this cross-section for you by calculating the moments of inertia $I_{xx}$ and $I_{yy}$. Unfortunately, they forgot to label them and have forgotten which value belongs to each axis. Determine which value is $I_{xx}$ and $I_{yy}$ and provide sufficient justification for your selection. The two values are: $1.8tL^3$ and $0.27tL^3$.

2. Calculate the product moment of inertia for the stiffener cross-section for the provided xy-axis system. Make sure to clearly communicate your solution approach to do this.

3. For the moment, $M$ , aligned in the horizontal direction as illustrated at the beginning of the question, calculate the magnitude of the largest bending stress in the cross-section as a function of $M$, $L$, and $t$, and indicate the location where it occurs.

````{solution} exam_bending_1
:class: dropdown

::::{tab-set}
:::{tab-item} Final Answer

1. $I_{xx} = 1.8tL^3$ and $I_{yy} = 0.27tL^3$

2. $I_{xy} = 0.123tL^3$

3. $\sigma_{max} = 0.72 \frac{M}{tL^2}$ and occurs at point 1

:::

::::
````

## Sample Exam Question 2

````{exercise} 
:label: exam_bending_2

Consider the cantilever beam $ABCD$ illustrated below left with a fixed support at $A$, a uniform distributed load of $w = 5~kN/m$ acting from $B$ to $C$, and a moment couple $M_D = 12~kNm$ acting at $D$. The thin-walled constant-thickness cross-section of the beam is illustrated below right. Answer the following questions in relation to this beam, loading, and beam cross-section.

```{figure} ./Figures/hw_bending_2.svg
:alt: Unsymmetric cantilever beam ABCD with complex loading and thin-walled cross-section illustrated. 
:width: 90%
:align: center
```
````

1. Using thin-walled approximations, calculate $I_{xx}$, $I_{yy}$, and $I_{xy}$ as functions of the cross-section parametric dimensions. This must be done for the coordinate system and orientation given in the above figure.

2. Determine the location and value of the maximum internal bending moment that will occur along the length of the beam. Please make sure to provide sufficient motivation/calculation to support your identification of the location and value of the maximum bending moment. This could, for instance, be in the form of generating and using an internal moment diagram. 

3. A colleague of yours has completed the primary sizing of the beam cross-section ($a = 20~mm$) and updated the moments of inertia for you as functions of thickness $t$ below. Using these updated properties and your results from part 2), calculate the minimum thickness $t$ required to prevent yielding of the beam cross-section if the material has a yield stress $\sigma_y = 150~MPa$.

$I_{xx} = \left( 9.58 \times 10^6 mm^3 \right)t$, $I_{yy} = \left( 1.03 \times 10^6 mm^3 \right)t$, $I_{xy} = \left( -8.91 \times 10^5 mm^3 \right)t$


````{solution} exam_bending_2
:class: dropdown

::::{tab-set}
:::{tab-item} Final Answer

1. $I_{xx} = 335.3a^3t$, $I_{yy} = 36a^3t$, and $I_{xy} = -31.2a^3t$

2. $M_{max} = 12~kNm$

3. $t_{min} = 3.6~mm$ 

:::
:::{tab-item} Intermediate Answers
text

:::

::::
````

