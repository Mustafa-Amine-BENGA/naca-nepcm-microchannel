# Thermo-hydraulic study of a NEPCM micro-channel with an oscillating NACA 0012 airfoil

2D unsteady CFD study (Ansys Fluent) of a heated micro-channel for electronics cooling. Two enhancement strategies are assessed: an oscillating NACA 0012 airfoil acting as an active mixer (sliding mesh), and nano-encapsulated phase change materials (NEPCM) added to water.

VIDEO_HERE

*Velocity and streamlines (top), temperature (middle) and specific heat of the mixture (bottom), θ₀ = 15°, St = 0.3, φ = 0.04.*

## Key findings
- At equal velocity, the airfoils raise heat transfer by a few percent but nearly double the pressure drop: the performance evaluation criterion stays below 0.9.
- The pressure drop is set by the presence of the airfoils, not by their motion; the actuation power is negligible.
- The oscillation amplitude is the most effective parameter; among the frequencies tested, St = 0.3 performs best.
- NEPCM degrade performance: only about 20 % of the capsules melt, while their effect on viscosity applies to the whole flow.

## Method
- Ansys Fluent 2026 R1, laminar, unsteady, sliding mesh (structured mesh, 85,700 cells)
- Temperature-dependent mixture properties implemented in a C user-defined function ([`udf/UDF_NEPCM.c`](udf/UDF_NEPCM.c))
- Sliding-mesh method validated against Kurtulus (NACA 0012, Re = 1000)
- Mesh and time-step convergence verified with the GCI method (Celik et al., 2008)

## Report
- [English](report/report_EN.pdf)

## Author
Mustafa Amine BENGA
