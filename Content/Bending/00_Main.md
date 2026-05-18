---
kernelspec:
  name: python3
  display_name: Python 3
---

# Bending Exercises
Some introductory text goes here.

```{code-cell} python
:tags: [remove-input]
# Data for plotting
t = np.arange(0.0, 2.0, 0.01)
s = 1 + np.sin(2 * np.pi * t)

fig, ax = plt.subplots()
ax.plot(t, s)

ax.set(xlabel='time (s)', ylabel='voltage (mV)',
       title='Waves in Time')
ax.grid()

fig.savefig("test.png")
plt.show()
```

Divider text

```{pyodide}
print("Hello from Pyodide")
```

Divider text

```{code-cell} python
import numpy as np
import matplotlib.pyplot as plt

# Create x values in degrees
x_deg = np.linspace(0, 180, 500)

# Convert degrees to radians for the sine function
x_rad = np.radians(x_deg)

# Compute the function
y = np.arctan(
    ((2/3) * np.sin(x_rad) * np.cos(x_rad)) /
    ((1/6) + 2*(np.cos(x_rad)-(1/2))**2 + (2/3) * np.cos(x_rad)**2)
)

# Convert result to degrees (optional)
y_deg = np.degrees(y)

# Create the plot
plt.figure(figsize=(8, 4))
plt.plot(x_deg, y_deg)

# Labels and title
plt.xlabel('$\theta$ (degrees)')
plt.ylabel('$\beta$ (degrees)')
plt.title(r'Plot of $\beta$ vs $\theta$')

# Grid
plt.grid(True)

# Show the plot
plt.show()
```