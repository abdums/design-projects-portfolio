# A2 – Truss Stress Analysis

## Objective

The objective of this assignment was to design a lightweight planar truss using A500 structural steel while satisfying the required geometry, loading, safety factor and pin-connection requirements. The truss was analyzed using static equilibrium, normal stress and shear stress calculations. A CAD model was then created in Creo to verify the geometry and compare its predicted weight with the analytical calculations.

---

## Analyze

### Design Setup

I selected a load of P = 20kN with the required dimensions a = 0.4m and b = 0.3m. I developed a four-joint, five-member truss using members AB, BC, CD, AD and AC. This geometry kept the structure simple while providing a stable truss that could support the required loads.

![Truss design and dimensions](../A02/images/1%20A2%20design.jpg)


### Truss Force Analysis

I analyzed the truss to determine the force carried by each member. I first treated the entire structure as a free body to determine the support reactions and then used the method of joints to solve the internal forces. The analysis showed that member AC carried the largest internal force at 37.97 kN in compression.

#### Overall Free-Body Diagram

![Overall free-body diagram](../A02/images/2%20A2%20force%201.png)


#### Support Reactions

![Support reaction calculations](../A02/images/3%20A2%20force%202.png)

#### Joint Geometry

![Member geometry calculations](../A02/images/4%20A2%20force%203.png)

#### Method of Joints

![Joint B and D calculations](../A02/images/5%20A2%20force%204.png)

![Joint C and A calculations](../A02/images/6%20A2%20force%205.png)

#### Member Force Results

![Member force results](../A02/images/7A2%20force%206.png)

### Truss Member Size

I sized all truss members using the largest calculated internal force because every member was required to have the same cross-sectional area. Using the 37.97 kN compression force in member AC, A500 Grade C steel and a safety factor of 3.5, I calculated a minimum required area of 385.2 mm². I selected a 20 mm × 20 mm cross section, producing an actual area of 400 mm².

![Minimum member area](../A02/images/8%20A2%20member%20size%201.png)

![Selected cross section](../A02/images/9%20A2%20member%20size%202.png)

### Analytical Truss Weight

I estimated the truss weight using the selected 400 mm² cross-sectional area and the combined length of all five members. The total member length was 3.454 m. Using a steel density of 7850 kg/m³, I calculated an approximate truss mass of 10.85 kg and weight of 106.4 N.

![Truss weight calculations](../A02/images/10%20A2%20truss%20weight.png)

### Pin Design

I designed four identical pins using the largest calculated truss force and modeled each connection in single shear. Hardened tool steel with a shear yield strength of approximately 1172 MPa and a safety factor of 4 was used. The minimum calculated pin diameter was 12.85 mm, so I selected a diameter of 13 mm.

![Pin design knowns](../A02/images/11%20A2%20pin%201.png)

![Pin shear calculations](../A02/images/12%20A2%20pin%202.png)

![Selected pin dimensions](../A02/images/13%20A2%20pin%203.png)


### CAD Model

The truss was modeled in Creo as one planar truss component rather than assembling every truss member separately. The model used a 20 mm × 20 mm member cross section and four 13 mm diameter pins. Material properties were assigned to the truss and pins so that Creo could calculate the mass of the completed assembly.

![Dimensioned Creo sketch](../A02/images/14%20A2%20SKETCH.png)

![Completed truss model](../A02/images/15%20A2%20TRUSS%20PART.png)

![Completed truss assembly](../A02/images/16%20A2%20ASSEMBLY.png)

### CAD Mass Comparison

The analytical and CAD results were reasonably close. The difference is expected because the hand calculation treated the members as ideal constant-cross-section elements, while the CAD model included the actual joint geometry and material removed by the pin holes.

![Creo mass properties](../A02/images/17%20A2%20MASS%20PROPERTIES.png)

---

### MEGR 2157 – Failure Mode Analysis

I investigated additional failure modes that were not included in the original member-sizing calculation. The analysis considered yielding, fracture and buckling for the truss members and shear failure for the connecting pins. The calculations showed that the tensile members are more likely to yield before fracture, while the long compression member AC is susceptible to buckling.

#### Truss Member Failure Modes

![MEGR 2157 material properties and stress setup](../A02/images/18-2157-material-properties.png)

![MEGR 2157 tension member analysis](../A02/images/19-2157-tension-members.png)

![MEGR 2157 compression member buckling analysis](../A02/images/20-2157-buckling.png)

#### Failure Mode Summary

The table below summarizes the loading, calculated stress, expected failure mode and possible design improvement for each truss member.

![Truss member failure mode summary](../A02/images/21-2157-failure-table.png)

#### Pin Connection Failure

The pin connection was evaluated using the selected 13 mm diameter and the required safety factor of 4. The calculated shear stress of 286.1 MPa remained below the allowable shear stress of approximately 293 MPa, so the selected pin satisfies the requirement. Because the design is close to the allowable value, increasing the diameter provides additional resistance to shear failure.

![MEGR 2157 pin failure analysis](../A02/images/22-2157-pin-analysis.png)

#### Pin Design Modification

Increasing the pin diameter from 13 mm to 14 mm increases the cross-sectional area and reduces the calculated shear stress to approximately 246.7 MPa. This lowers the likelihood of shear failure while preserving the same basic pin-connection design.

![MEGR 2157 pin design modification](images/23-2157-pin-modification.png)


## Decide
_Which geometry did you select and why? This is your first open design choice in the course — defend it._

### Geometry Selection

I selected a four-joint, five-member truss consisting of AB, BC, CD, AD and AC. I chose this geometry because it produced a stable and statically determinate structure while using a small number of members. The simple geometry also reduced the complexity of both the method-of-joints calculations and the CAD model while satisfying the required joint locations.

### Member Cross-Section Selection

The theoretical minimum cross-sectional area was 385.2 mm². Rather than using an unusual exact dimension, I selected a 20 mm × 20 mm square section with an area of 400 mm². This provided slightly more area than required while keeping the dimensions simple to manufacture and model.

### Pin Size Selection

The calculated minimum pin diameter was 12.85 mm. I selected a 13 mm diameter because it exceeded the minimum requirement while remaining close to the calculated optimum. All four pins were kept identical as required by the design constraints.

---

## Communicate

### Engineering Lessons Learned

This project demonstrated that designing for normal stress alone does not necessarily identify the most critical failure mechanism. The initial member sizing showed that the selected 20 mm × 20 mm section satisfied the yield-strength requirement, but the MEGR 2157 failure-mode investigation showed that the long compression member AC could instead be vulnerable to buckling. I also learned how analytical calculations and CAD mass properties can be used together to verify a design, with the analytical and Creo weight predictions differing by only about 2.93%.

### Mistakes and Design Changes

One important realization during the design process was that the dimensions shown in the assignment figure represented the horizontal locations of the joints rather than the lengths of the diagonal members. After correcting the interpretation of the geometry, the final truss used the required 0.4 m horizontal spacing and 0.3 m vertical spacing. I also initially sized the members only for normal stress, but the later failure-mode analysis demonstrated why compression-member buckling should also be considered in a complete structural design.

### Project Time

Total time from start to finish:

**13 hours**

### CAD Files

[Download the completed A2 Creo CAD files](files/Abdu%20A2%20CAD%20FILE.zip)
