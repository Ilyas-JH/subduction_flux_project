# Subduction Flux Calculation from Plate Reconstruction Models

This repository contains a code that be used to compute the subduction flux from plate reconstruction models. It is  It uses a simplified model of subduction : we consider that a slab has a constant given thickness and density of respectively $100km$ and $3g/cm^3$, and is sinking at the same velocity as the velocity of the subducting plate at the trench projected on the normal unit vector to the trench. The subduction flux is evaluated for a given subduction segment following this formula:

$F_{seg} = h w \rho \ | \vec{V} \cdot \vec{n} |$

With $h$ the thickness of the slab, $\rho$ its density, $w$ the width of subduction segment, $\vec{V}$ the absolute velocity of the plate at the midpoint of the segment and $\vec{n}$ the normal to the segment. Note that we take the absolute value of the dot product between $\vec{V}$ and $\vec{n}$ because the flux should always be positive no matter the orientation of $\vec{n}$ with respect to $\vec{V}$.

This is summerized in the following diagram.

<img src="subduction_flux_diagram.png" alt="fishy" class="bg-primary mb-1" width="500px">

This is a simple approach to the problem of calculating the subduction flux but it can be built-on to add complexity to the computation by for example adding an age grid to estimate the thickness of the sinking plate using a half-space cooling model.

The input should be GPlates files: .gmpl dynamic polygon file and .rot rotation file. The code is made to work with the following formmatting for the GPlates file location:
````{verbatim}
home/plate_models/key/key_rotation_model.rot
````
and
````{verbatim}
home/plate_models/key/key_dynamic_polygons.gpml
````
with key being a shorter name for a plate model, for example MA16 for Matthews et al. (2016). An example is given in the code for 4 plate models.

This code was written and tested with the version 1.0.0 of pyGPlates but it should work with versions higher than 0.47.


This work was done by Ilyas Jaah and Jhanvee Khanna for their tutored project as part of their M2 at IPGP. It was supervised by Boris Robert and Marianne Greff-Lefftz.
