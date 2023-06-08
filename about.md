---
include_sidebar: false
permalink: /about.html
title: about
url: about.html

---

{% include about.md %}

The CLOVER energy system model has the following modules with related functionality and input requirements:

**Solar PV**
The CLOVER Solar PV module takes inputs including location, orientation and tilt of array, and degradation rate. If running a simulation rather than an optimisation then additionally the size of the array. The CLOVER model directly extracts hourly predicted electricity generation estimates from the [Renewables.ninja](Renewables.ninja) model API for the array specification. 

**Battery Storage**
CLOVER can simulate or optimise for off-grid systems that inlcude battery storage. The model takes inputs to define the storage including battery lifetime, number of cycles, charging and discharging C-rates, or leakage. The storage size can be determined by the user for simulation.

**Diesel**
There are two modes for including diesel generation in the model: back-up or dispatched. In the back-up mode, the model adopts a load following approach for timesteps that are unmet by other sources of energy. In the dispatched mode, the diesel generator can be programmed to come on under certain conditions (battery state of charge) and will charge the batteries as well as meet demand directly. The model can auto size the diesel generator based on the demand profile; or the user can specify the size of the generator. Other inputs include fuel consumption and minimum load factors.

**Grid** 
The CLOVER model can be configured so that electricity systems can have a grid connection. For contexts where the grid is unreliable, the Grid module can be used to produce a grid availability profile. The model can be configured to prioritise either generation from the grid, or from the system being modelled. 

**Load**
The CLOVER model has a load module that permits stochastic modelling of hourly load profiles based on the number of devices, time of use of devices, number of devices within the community and the anticipated growth in number of devices over the modelling time horizon. Alternatively, the user can provide an hourly profile or profiles for community, business or institutional loads.

**PVT**

**Solar Thermal**





