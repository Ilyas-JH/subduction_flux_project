# Subduction Flux Calculation from Plate Reconstruction Models

This code can be used to compute the subduction flux from plate reconstruction models. It uses a simplified model of subduction : we consider that a slab has a constant given thickness and density of respectively $100km$ and $3g/cm^3$, and is sinking at the same velocity as the velocity of the subducting plate at the trench projected on the normal unit vector to the trench.

```{figure} ../subduction_flux_diagram.png
---
height: 150px
name: directive-fig
---
Here is my figure caption!
```

This is a simple approach to the problem of calculating the subduction flux but it can be built-on to add complexity to the computation by for example adding an age grid to estimate the thickness of the sinking plate using a half-space cooling model.

The input should be GPlates files: .gmpl dynamic polygon file and .rot rotation file. 

This code was written and tested with the version 1.0.0 of pyGPlates but it should work with versions higher than 0.47.
