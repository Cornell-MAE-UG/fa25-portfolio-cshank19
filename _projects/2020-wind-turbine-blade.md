---
layout: project
title: Wind Turbine Blade Design Project
description: Class project to design most effective blades for a wind turbine
technologies: [MATLAB, CAD, Wind Tunnel, LabVIEW]
image: /assets/images/Wind_turbine_physical.png
---


We were asked to design blades for a small wind turbine. The blades had to be designed to maximize power extraction from the wind and be structurally sound. More specifically, the blades could have a maximum length of 6’’, interface properly with the wind turbine hub, and must not exceed the material’s flexural strength of 55MPa. Our design had to fulfill these constraints in order to attach to the wind turbine hub, fit inside the wind tunnel, and operate safely without failure in the parts. 


The design variables we chose to optimize were the length, twist, and taper of the blades. The first step in the process was selecting an airfoil profile; we chose NACA 4415. Next the optimal angle of attack for the airfoil was determined by analyzing the CL/CD versus angle of attack, which was at 9 degrees. To define the twist, we aimed to maintain the optimal AoA for a wind speed 7 m/s and 2000 RPM operational speed for the turbine. By performing a free body diagram analysis an airfoil, the following function was derived: $\theta(r) = \arctan(\frac{u_{wind}}{rw}) - \alpha$. This equation captures how the total wind vector changes along the length of the blade and adjusts the pitch accordingly. 

With the twist determined, only the taper was left to design. A Matlab script was developed following conservation laws on a control volume analysis to calculate the bending stress along a blade based on the length and chord length along the length. This script helped ensure that our blade design would not fail under load in the wind tunnel. Another Matlab script was developed that performed parameter analysis on an exponential function to find an equation that satisfied both structural integrity and maximized useful force produced by the blades. The result is the following equation $c(r) = \exp{-.5*frac{r}{R}}$, where R is max radius. 

These equations were then used to make splines in Autodesk Fusion, which the airfoil profile was extruded over. The two images below show the final design of the blades in CAD. 

Once the blades were 3D printed, testing was performed in the wind tunnel named “Big Blue”. The goal of the testing was to generate power curves at different wind speeds to characterize optimal operating speed, omega, and analyze maximum power output. To generate the power curves the following operations were performed multiple times:
    1.Set wind speed
    2.Ensure torque brake voltage is zeroed
    3.Slightly increase voltage of the torque brake
    4.Wait a short time to allow the system to reach steady state
    5.Record RPM of wind turbine
    6.Repeat steps 3-5 until turbine stalls 

The results were the following power curves shown in the image below. At higher wind speeds, we were unable to stall the wind turbine with the maximum torque from the torque brake, leading to incomplete power curves. However, this is a positive indication that the blades were well designed as they are able to effectively generate lift and have potential to generate high power output.

This was done as a group project including me and three other students. My contributions to the project were developing the Matlab script to calculate bending stress along the blade, assist in deriving equations from free body diagrams, and perform testing. 



