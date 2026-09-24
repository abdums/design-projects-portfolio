
# A5 – Bracket Design

## Objective

The objective of this assignment was to design a metal bracket capable of supporting a polyester strap and connecting to the rigid T-beam shown in the assignment.

The bracket was divided into five structural features, A through E, to simplify the analysis.

Each feature was analyzed using strength and stiffness equations to determine the required dimensions.

The selected material was ASTM A36 steel, with an applied strap force of 650 lbf, a safety factor of 4 and a maximum allowable deflection of 0.005 in per feature.

The calculations were completed by hand using simplified beam and axial loading models.

---

## Analyze

### 1. Design Setup and Material Selection

ASTM A36 steel was selected as the material for the bracket.

The design requirements, material properties and allowable stress were established before beginning the structural analysis.

![Design Setup and Material Selection](images/Page01.png)

### Load Path

The polyester strap applies two equal forces to the cylindrical support.

The total applied load was determined and used to establish the load path through the bracket.

The selected material properties and calculated loading conditions are shown below.

![Load Path and Material Properties](images/Page02.png)

### Simplifying Assumptions

Several simplifying assumptions were made to allow the bracket to be analyzed using fundamental strength-of-materials equations.

The bracket was assumed to be symmetrically loaded and the applied load was considered static.

Direct shear failure and shear deflection were neglected as instructed in the assignment.

![Simplifying Assumptions](images/Page03.png)

---

### 2. Feature A – Cylindrical Strap Support

Feature A is the cylindrical member that supports the polyester strap.

It was approximated as a cantilever beam with an equivalent uniformly distributed load.

The required cylinder diameter was determined using bending stress and stiffness analysis.

#### Free-Body Diagram and Stress Analysis

The maximum bending moment was determined from the applied strap load.

The bending stress equation was then solved symbolically and numerically to determine the minimum required diameter.

![Feature A Stress Analysis](images/Page04.png)

#### Stiffness Analysis and Final Selection

The cylinder was also analyzed using the maximum allowable deflection.

The resulting dimensions were compared and the stress requirement controlled the selected diameter.

![Feature A Stiffness Analysis and Final Selection](images/Page05.png)

---

### 3. Feature B – Vertical Connecting Member

Feature B transfers the load from the cylindrical support into the upper bracket.

It was approximated as an axially loaded rectangular member.

The required thickness was determined using normal stress and axial deformation equations.

#### Knowns, Unknowns and Free-Body Diagram

The load transferred from Feature A was used to establish the loading conditions for Feature B.

![Feature B Setup and FBD](images/Page06.png)

#### Stress and Stiffness Analysis

The required thickness was calculated independently from the stress and stiffness requirements.

![Feature B Stress and Stiffness Analysis](images/Page07.png)

#### Final Selection

The calculated dimensions were compared and the stress requirement controlled the final thickness.

![Feature B Final Selection](images/Page08.png)

---

### 4. Feature C – Lower Bracket Support

Feature C transfers the load from the vertical connecting member toward the upper bracket.

It was modeled as a simply supported beam with a concentrated load at its center.

Symmetry was used to determine the support reactions.

#### Knowns, Assumptions and Free-Body Diagram

The total load transferred from Feature B was used to determine the reactions at the two supports.

![Feature C Setup and FBD](images/Page09.png)

#### Stress and Stiffness Analysis

The maximum bending moment was determined, followed by the required thickness from bending stress and deflection.

![Feature C Stress and Stiffness Analysis](images/Page10.png)

#### Final Selection

The stress-based and stiffness-based dimensions were compared.

The stress requirement controlled the selected thickness of Feature C.

![Feature C Final Selection](images/Page11.png)

---

### 5. Feature D – Upper Bracket Support

Feature D represents one of the upper structural features that transfers the load toward the rigid T-beam.

The load was determined using the symmetric support reactions obtained from Feature C.

A simplified axial loading model was used to determine its required dimensions.

#### Knowns, Assumptions and Free-Body Diagram

![Feature D Setup and FBD](images/Page12.png)

#### Stress and Stiffness Analysis

The required width was determined using axial stress and deformation equations.

![Feature D Stress and Stiffness Analysis](images/Page13.png)

#### Final Selection

The calculated dimensions were compared and the stress requirement controlled the selected width.

![Feature D Final Selection](images/Page14.png)

---

### 6. Feature E – Upper T-Bracket Feature

Feature E represents the remaining upper structural feature of the bracket.

The same symmetric load distribution was used to establish its loading conditions.

The member was approximated as an axially loaded rectangular section.

#### Knowns, Assumptions and Free-Body Diagram

![Feature E Setup and FBD](images/Page15.png)

#### Stress and Stiffness Analysis

The required thickness was determined independently using normal stress and axial deformation equations.

![Feature E Stress and Stiffness Analysis](images/Page16.png)

#### Final Selection

The calculated dimensions were compared and the stress requirement controlled the selected thickness.

![Feature E Final Selection](images/Page17.png)

---

## Decide

### 7. Design Selection

The stress and stiffness analyses were compared to determine the required dimensions of each structural feature.

For the simplified analytical models, the stress requirements controlled the selected dimensions of all five features.

The stress-based dimensions were therefore used as the basis for the preliminary bracket design.

The design was kept symmetric where possible to simplify the loading conditions and reduce the number of independent calculations.

The resulting dimensions are shown in the handwritten calculations and multiview sketches.

---

### 8. Multiview Sketches

Two separate preliminary multiview sketches were prepared to illustrate the dimensions obtained from the stress and stiffness analyses.

Both sketches use the same general bracket geometry, allowing the differences between the calculated dimensions to be compared.

#### Stress-Based Multiview Sketch

The first sketch illustrates the bracket using the minimum dimensions obtained from the stress analysis.

![Stress-Based Multiview Sketch](images/Page18.png)

#### Stiffness-Based Multiview Sketch

The second sketch illustrates the bracket using the minimum dimensions obtained from the stiffness analysis.

![Stiffness-Based Multiview Sketch](images/Page19.png)

The sketches illustrate the preliminary analytical geometry. The final T-beam fit dimensions and manufacturing tolerances have not been incorporated.

---

## Communicate

### 9. Design Process

The design began by reviewing the assignment requirements and selecting ASTM A36 steel as the material.

The bracket was divided into five structural features to simplify the analysis.

The load applied by the polyester strap was determined first and then transferred through the remaining features.

For each feature, the knowns, unknowns, assumptions and free-body diagram were established before solving the stress and stiffness equations.

The resulting dimensions were compared to identify the governing design requirement.

Finally, two preliminary multiview sketches were prepared to communicate the stress-based and stiffness-based designs.

---

### 10. Lessons Learned

#### Governing Design Criterion

The stress requirement controlled the calculated dimensions of all five features.

Feature A demonstrated a particularly noticeable difference between the dimensions required by stress and stiffness.

The stress analysis required a cylinder diameter of approximately 1.033 in, while the stiffness analysis required approximately 0.527 in.

This demonstrated that satisfying the stiffness requirement alone does not guarantee that a component will satisfy the required strength and safety factor.

#### Error Propagation

The calculations demonstrated how a value obtained from one feature can affect the dimensions of subsequent features.

The total strap load was first determined for Feature A and then transferred through Feature B into Feature C.

The support reactions from Feature C were subsequently used to analyze Features D and E.

An incorrect load calculation in an earlier feature would therefore affect the dimensions calculated for the remaining features.

Maintaining a consistent load path and checking the reaction forces helped reduce the risk of carrying an incorrect load into the following calculations.

#### Assumption Sensitivity

One important assumption was that the bracket was symmetrically loaded.

This allowed the total load to be divided equally between the two upper supports.

If the loading were not symmetric, the reactions would be different and the dimensions of Features D and E would need to be recalculated.

The simplified axial and beam models also neglect local stress concentrations and connection effects. Additional analysis would be needed to verify the complete bracket under actual operating conditions.

---

### 11. Completion and Reflection

This assignment provided additional practice in connecting statics and strength-of-materials calculations to a structural design.

It reinforced the importance of defining assumptions, using consistent dimensions and tracing loads through connected structural features.

Due to time constraints, the additional MEGR 2157 linkage and fit-selection requirements were not completed.

The submitted work documents the five preliminary feature analyses and the two multiview sketches.

**Total Time:** 5 Hours

---

### 12. References

1. ASTM A36 Steel – Material Properties, MatWeb Materials Database.

2. Machinery's Handbook, 31st Edition – Beam Stress, Deflection and Limits and Fits.

3. [Uline – Heavy-Duty Polyester Cord Strapping](https://www.uline.com/Product/Detail/S-12925/Poly-Cord-Strapping/Heavy-Duty-Polyester-Cord-Strapping-3-4-x-2500)

4. MEGR 2157 – A5 Bracket Design Assignment, Appendices A–E.