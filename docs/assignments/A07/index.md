# A7 - Finite Element Analysis of Bracket

## Objective

The objective of this assignment was to improve my previous bracket design using finite element analysis in SOLIDWORKS. I compared three versions of the bracket by examining stress, displacement, safety factor and mass. I used the simulation results to decide where the geometry needed reinforcement.

## Analyze

### Simulation Setup

I used a static simulation with the assigned ASTM A36 steel material. The inside faces of the two upper mounting tabs were fixed and a downward load was applied to the lower cylindrical feature. I kept the material and loading setup consistent when comparing the three designs.

<figure>
  <img src="images/d_1_fixture.png" alt="Fixed geometry on the upper mounting tabs" width="560">
  <figcaption>Figure 1. Fixed surfaces on the bracket mounting tabs.</figcaption>
</figure>

<figure>
  <img src="images/external_load_d_1.png" alt="External loading on the lower cylinder" width="560">
  <figcaption>Figure 2. Applied load on the lower cylindrical feature.</figcaption>
</figure>

### Design I - Original Bracket

Design I used the original bracket geometry without additional reinforcement. I ran the simulation using coarse, medium and fine meshes. The largest stress occurred near the connection between the vertical support and the main bracket. The lower cylinder also experienced substantial displacement.

<figure>
  <img src="images/d_1_mesh.png" alt="Design I mesh" width="560">
  <figcaption>Figure 3. Initial mesh for Design I.</figcaption>
</figure>

<figure>
  <img src="images/max_stress_3.png" alt="Design I fine mesh stress result" width="560">
  <figcaption>Figure 4. Design I maximum stress using the fine mesh.</figcaption>
</figure>

<figure>
  <img src="images/max_displacement_3.png" alt="Design I fine mesh displacement result" width="560">
  <figcaption>Figure 5. Design I displacement using the fine mesh.</figcaption>
</figure>

<figure>
  <img src="images/minimum_sf_3.png" alt="Design I fine mesh safety factor result" width="560">
  <figcaption>Figure 6. Design I safety factor using the fine mesh.</figcaption>
</figure>

I compared the three mesh results to check how sensitive the results were to element size. Stress and safety factor did not converge within seven percent, so I used the fine mesh results after the third attempt, as allowed by the assignment.

<figure>
  <img src="images/Page1v2.png" alt="Handwritten Design I convergence calculations" width="650">
  <figcaption>Figure 7. Design I handwritten mesh convergence calculations and proposed improvements.</figcaption>
</figure>

[Download Design I CAD files](files/a7_design_1.zip)

### Design II - Added Support and Fillets

For Design II, I strengthened the vertical support and added fillets at the connections between the support, main bracket and lower cylinder. These changes were intended to reduce bending and stress concentrations identified in Design I.

<figure>
  <img src="images/Design_2_v_support_mod.png" alt="Design II vertical support modification" width="560">
  <figcaption>Figure 8. Modified vertical support.</figcaption>
</figure>

<figure>
  <img src="images/fillet_B_and_C_connection.png" alt="Fillet between bracket features B and C" width="560">
  <figcaption>Figure 9. Fillet added at the support connection.</figcaption>
</figure>

<figure>
  <img src="images/fillet_cylinder_support_connection.png" alt="Fillet between cylinder and support" width="560">
  <figcaption>Figure 10. Fillet at the cylinder and support connection.</figcaption>
</figure>

<figure>
  <img src="images/Design_2_overall_change.png" alt="Overall Design II geometry" width="560">
  <figcaption>Figure 11. Overall Design II geometry.</figcaption>
</figure>

The revised geometry reduced maximum stress and displacement compared with Design I. The stress, displacement and safety factor results were within seven percent between the medium and fine meshes.

<figure>
  <img src="images/design_2_max_stress_test_3.png" alt="Design II fine mesh stress" width="560">
  <figcaption>Figure 12. Design II maximum stress using the fine mesh.</figcaption>
</figure>

<figure>
  <img src="images/design_2_max_displacement_test_3.png" alt="Design II fine mesh displacement" width="560">
  <figcaption>Figure 13. Design II maximum displacement using the fine mesh.</figcaption>
</figure>

<figure>
  <img src="images/design_2_minimum_sf_3.png" alt="Design II fine mesh safety factor" width="560">
  <figcaption>Figure 14. Design II safety factor using the fine mesh.</figcaption>
</figure>

<figure>
  <img src="images/Page2.png" alt="Handwritten Design II convergence calculations" width="650">
  <figcaption>Figure 15. Design II handwritten mesh convergence calculations.</figcaption>
</figure>

[Download Design II CAD files](files/a7_design_2.zip)

### Design III - Triangular Gussets

Design III added triangular gussets between the main bracket and lower support. The gussets create additional paths for transferring force and reinforce the region that experienced high stress in the earlier designs.

<figure>
  <img src="images/d_3_mod_support.png" alt="Design III modified support" width="560">
  <figcaption>Figure 16. Design III modified support.</figcaption>
</figure>

<figure>
  <img src="images/d_3_gussets.png" alt="Design III triangular gussets" width="560">
  <figcaption>Figure 17. Triangular gussets added to the bracket.</figcaption>
</figure>

Design III produced the lowest maximum stress and highest safety factor of the three designs. Its displacement was lower than Design I but higher than Design II. Stress and safety factor did not converge within seven percent, so I used the fine mesh results after three attempts.

<figure>
  <img src="images/d_3_max_stress_3.png" alt="Design III fine mesh stress" width="560">
  <figcaption>Figure 18. Design III maximum stress using the fine mesh.</figcaption>
</figure>

<figure>
  <img src="images/d_3_max_displacement_3.png" alt="Design III fine mesh displacement" width="560">
  <figcaption>Figure 19. Design III maximum displacement using the fine mesh.</figcaption>
</figure>

<figure>
  <img src="images/d_3_min_sf_3.png" alt="Design III fine mesh safety factor" width="560">
  <figcaption>Figure 20. Design III safety factor using the fine mesh.</figcaption>
</figure>

<figure>
  <img src="images/Page3.png" alt="Handwritten Design III convergence calculations" width="650">
  <figcaption>Figure 21. Design III handwritten mesh convergence calculations.</figcaption>
</figure>

[Download Design III CAD files](files/a7_design_3_with_gussets.zip)

## Decide

### Comparison of the Three Designs

The table below summarizes the fine mesh results used for the final comparison.

| Result | Design I | Design II | Design III |
| --- | ---: | ---: | ---: |
| Maximum stress in MPa | 2487 | 642.6 | 159.3 |
| Maximum displacement in mm | 2.570 | 0.3164 | 0.6403 |
| Minimum safety factor | 0.1005 | 0.3890 | 1.569 |
| Mass in lb | 1.22 | 1.24 | 1.29 |
| Number of elements | 55616 | 56107 | 58331 |

The maximum stress was located near the upper connection of the vertical support in Designs I and II. In Design III, it was located near the reinforced connection between the cylinder and the support. Maximum displacement occurred at the outer end of the lower cylinder in all three designs.

<figure>
  <img src="images/Page4.png" alt="Handwritten final design comparison" width="650">
  <figcaption>Figure 22. Handwritten comparison of the three designs.</figcaption>
</figure>

### Design Selection

I selected Design III as the strongest of the three tested versions because it had the lowest maximum stress and the highest minimum safety factor. The tradeoff was slightly higher mass and greater displacement than Design II. Although Design III showed a major improvement over the original bracket, its safety factor was still below the target of four from the original design assignment. Further improvements and validation would be needed before considering it acceptable for that target.

## Communicate

### Lessons Learned

This assignment showed me how finite element analysis can identify areas of a design that need reinforcement. Increasing the thickness of a support and adding fillets reduced stress, while triangular gussets helped distribute the load more effectively. I also learned that a finer mesh can change the reported maximum stress even when displacement changes only slightly. These differences must be checked before relying on simulation results to make a design decision.

One limitation was that not all results converged within seven percent after three meshes. This means the fine mesh results are useful for comparing the designs, but they still have uncertainty. Another lesson was that reducing stress does not always produce the lowest displacement or the lightest part.

### Time Spent

Actual time spent: **7 hours**

### CAD Files

- [Design I CAD download](files/a7_design_1.zip)
- [Design II CAD download](files/a7_design_2.zip)
- [Design III CAD download](files/a7_design_3_with_gussets.zip)
