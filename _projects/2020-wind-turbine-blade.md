---
layout: project
title: Wind Turbine Blade Design Project
description: Class project to design most effective blades for a wind turbine
technologies: [MATLAB, CAD, Wind Tunnel, LabVIEW]
image: /assets/images/function-graph.png
---


We were asked to design blades for a small wind turbine. The blades had to be designed to maximize power extraction from the wind and be structurally sound. More specifically, the blades could have a maximum length of 6’’, interface properly with the wind turbine hub, and must not exceed the material’s flexural strength of 55MPa. Our design had to fulfill these constraints in order to attach to the wind turbine hub, fit inside the wind tunnel, and operate safely without failure in the parts. 


The design variables we chose to optimize were the length, twist, and taper of the blades. The first step in the process was selecting an airfoil profile; we chose NACA 4415. Next the optimal angle of attack for the airfoil was determined by analyzing the CL/CD versus angle of attack, which was at 9 degrees. To define the twist, we aimed to maintain the optimal AoA for a wind speed 7 m/s and 2000 RPM operational speed for the turbine. By performing a free body diagram analysis an airfoil, the following function was derived: 
```math
$\theta(r) = \arctan(\frac{u_{wind}}{rw})  \alpha$
```math


