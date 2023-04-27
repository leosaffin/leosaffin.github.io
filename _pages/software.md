---
layout: page
permalink: /software/
title: Software
description: Code I have worked on
nav: true
nav_order: 4
---


## **My Repositories**
---

### [iris-extensions](https://github.com/leosaffin/iris-extensions)
Most of the data analysis I do is in some way built on [iris](https://scitools-iris.readthedocs.io/en/stable/index.html). This is a library I have built up from various things I have done using iris. 

### [pylagranto](https://github.com/leosaffin/pylagranto)
This is a modified version of the [Lagranto](https://iacweb.ethz.ch/staff/sprenger/lagranto/) tool for calculating Lagrangian trajectories. I changed it so that I could calculate trajectories using model level data from the Met Office's Unified Model. It is essentially the same Fortran code for calculating trajectories but the main loop and reading data has been replaced with python code, so it is more flexible and easier to modify.

### [pygame-plot](https://github.com/leosaffin/pygame_plot)
A very simple plotting interface that I use to quickly browse through gridded data using the arrow keys and allows me to use matplotlib colour scales.

### [constrain](https://github.com/leosaffin/constrain)
Library for current work with code to calculate dynamical indices (e.g. eddy-feedbacks, North Atlantic Oscillation). I'm using CMIP6 and ERA5 data, but it should work for any gridded data.


&nbsp;

## **Contributions**
---
### [twin-otter](https://github.com/EUREC4A-UK/twin-otter)
A library of useful scripts for analysing and visualising data from the twin-otter aircraft which was part of the EUREC4A field campaign.

### [eurec4a-environment](https://github.com/eurec4a/eurec4a-environment)
A library of functions and scripts for calculating variables that describe the large-scale environment from observation taken during the EUREC4A field campaign

### [flight-phase-separation](https://github.com/eurec4a/flight-phase-separation)
YAML files describing the flights and flight segements during the EUREC4A field campaign. I generated the files for the twinotter flights [here](https://github.com/EUREC4A-UK/flight-phase-separation/tree/twinotter). They are not in the main repository yet because the data files are not openly available, so the automated testing required to put them in the main repository can't be done yet.

### [speedy.f90](https://github.com/samhatfield/speedy.f90)
This is Sam Hatfield's version of the SPEEDY model using more modern Fortran code. I used his older version for my work on reduced-precision computing in parametrizations, but this is in a private repository. I did help fix some issues with porting from Fortran77 to Fortran90 that made their way into this public repository as well though.

&nbsp;

## **Repositories for papers**
---
### [moisture-tracers](https://github.com/leosaffin/moisture_tracers)
Code used to produce results and figures in "[Kilometer-Scale Simulations of Trade-Wind Cumulus Capture Processes of Mesoscale Organization](https://doi.org/10.1029/2022MS003295)"

### [wcb-outflow](https://github.com/leosaffin/wcb_airmass)
Code used to produce results and figures in "[Circulation conservation in the outflow of warm conveyor belts and consequences for Rossby wave evolution](https://onlinelibrary.wiley.com/doi/10.1002/qj.4143)"

&nbsp;

## **Private Repositories**
---
### Diabatic tracers in the UM
During my PhD I worked a lot with potential vorticity (PV) and potential temperature ($\theta$) tracers. These tracers work by accumulating the tendencies in these variables from each parametrization at each timestep and advecting them as tracers. Because PV and $\theta$ are conserved by advection, each tracer gives the accumulated change in PV or $\theta$ due to a specific physical process over the course of a model run and a tracer of the initial field completes the budget. Initially I worked on a branch taken from Jeff Changnon. The tracers and my developments were then taken by Claudio Sanchez and fully incorparated in to the UM so that they are now available for anyone using the UM with minimal effort.

I have also more recently worked moisture tracers, the same idea but for specific humidity, which are not included in the main UM, but I have branches for versions 12.0 and 12.2. 

### Standalone CoMorph
CoMorph is a new convection parametrization in development at the Met Office. As part of my work on the ParaCon project, I took the standalone version of CoMorph and added an interface for using netCDF files so that I could run it from EUREC4A observations.
