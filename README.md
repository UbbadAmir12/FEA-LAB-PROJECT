# FEA-LAB-PROJECT
# **Finite Element Analysis of a Pentagon Structure Under Static and Transient Loading Conditions** 

**Name: UBBAD AMIR**

**Roll Number: ME-1884**

Course: Finite Element Analysis Lab

Software: ANSYS

**1. Introduction**

This project performs static and time-dependent (transient) finite element simulations on a simple pentagon geometry. The objective is to evaluate deformation and stress response under remote loading, and to validate the results through a mesh convergence study with an allowable convergence error of 5%. The transient study replaces the explicit dynamic approach and captures the time evolution of response under a transient load.

**2. Geometry and Material Properties**
   
**2.1 Geometry**

Geometry: Pentagon (simple 3D solid)

One face fully fixed

Force applied at 1/3rd of the fixed face (remote force point)

**2.2 Material Properties**

Material properties were modified as required:

Property	Value
Young’s Modulus (E)	84 GPa
Poisson’s Ratio (ν)	0.28
**3. Static Structural Simulation**

**3.1 Setup**

Simulation Type: Linear Static

Applied Remote Force: 2031 N

Fixed one pentagon face

Force applied at 1/3rd height of fixed face

Mesh Type: Tetrahedral elements

Convergence criterion: 5% allowable error

![1](https://github.com/user-attachments/assets/5cc3c791-b863-4d7e-af76-4622db2816af)


**3.2 Results**

Maximum Stress

**𝜎max=1.7097dyne/cm2**
(≈ 1.7097 × 10⁻¹ Pa)

![2](https://github.com/user-attachments/assets/2352201f-bfa3-4040-b814-3a2dca927254)

**General Observations**

Highest stresses observed at corners adjacent to the fixed face

Deformation concentrated near the free edge

Stress distribution symmetric and physically reasonable

**3.3 Mesh Convergence (Static)**

Multiple mesh densities were run

Stress values stabilized within a 5% difference, meeting the convergence requirement

Finer meshes showed negligible additional accuracy gain

![4](https://github.com/user-attachments/assets/7bcef962-f8fb-4e5f-a607-90523b0a22f0)


**4. Transient (Time-Dependent) Simulation**

**4.1 Setup**

Simulation Type: Transient (time-dependent)

Applied Force: 282 N 
Total simulation time: 1 s
Time step: 0.2 s
Boundary Conditions: Same fixed face as static case; apply time-varying load profile as a step or ramp according to your test plan

Material: E = 84 GPa, ν = 0.28

Mesh: Tetrahedral elements; refined in regions with high stress gradient
**
4.2 Results**

Maximum Deformation over 1 second:

**𝛿max=1.1027e−8m**

![5](https://github.com/user-attachments/assets/96d96cee-479f-4ff9-909c-c20031de610b)

Maximum Stress:
**𝜎max= 1160.8Pa**

![explicit](https://github.com/user-attachments/assets/32c627d7-66ab-4b9f-b404-94ce83eedf38)


**Observations**

Deformation values are extremely small due to the high stiffness of the material (E = 84 GPa).

Stress gradually builds up after load application and stabilizes as the structure reaches steady response.

Minor transient oscillations may be observed early in the simulation, characteristic of dynamic settling.

The structure remains well within the elastic limit under the 282 N transient loading.

**4.3 Mesh Convergence (Explicit)**

Performed refinement series for transient runs.

Peak deformation and peak stress values converged to within 5% between the last two refinements.

Final mesh accepted for report results.

**5. Discussion**
   
**Static vs. Transient Simulation Comparison**
**Static Simulation (2031 N load):**

Determines the final equilibrium deformation and stress under a much larger static force.

Maximum stress during static loading was 1.7097 dyne/cm² (≈1.7097 × 10⁻¹ Pa).

Highest stresses occur at corners close to the fixed face, with deformation at the free edge.

**Transient Simulation (282 N, 1 s, 0.2 s steps):**

Captures the time-dependent structural response, including the build-up of stress and small dynamic oscillations.

Maximum deformation recorded was 1.1027 × 10⁻⁸ m.

Maximum transient stress reached 1160.8 Pa, significantly higher than the static stress due to the different load application, rate effects, and transient response characteristics.

Stress stabilizes over time, indicating dynamic equilibrium is achieved.

**Overall Interpretation:**

Static analysis represents a final, steady-state condition.

Transient analysis reveals how the structure behaves over time, showing early oscillations and gradual stabilization.

Even though the transient load is smaller, its dynamic nature leads to a higher stress response (1160.8 Pa) compared to the small static stress value.

Both simulations confirm that the structure remains safely within elastic limits.
