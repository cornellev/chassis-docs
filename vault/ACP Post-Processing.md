
### Postprocessing

Postprocessing options include:  
[Total Deformation](https://ansyshelp.ansys.com/public//Views/Secured/corp/v251/en/acp_tut/acp_tut7_postprocess.html#acp-tut7-mech-deform)  
[Stress Plot](https://ansyshelp.ansys.com/public//Views/Secured/corp/v251/en/acp_tut/acp_tut7_postprocess.html#acp-tut7-stress-plot)  
[Composite Failure Tool](https://ansyshelp.ansys.com/public//Views/Secured/corp/v251/en/acp_tut/acp_tut7_postprocess.html#acp-tut7-mech-failure)  
[Composite Sampling Point Tool](https://ansyshelp.ansys.com/public//Views/Secured/corp/v251/en/acp_tut/acp_tut7_postprocess.html#acp_tut7_tttp_acppost)

### Commonly used Symbols for Composite Failure Tool (Failure modes):  
e = strain  
s = stress  
1 = material 1 direction  
2 = material 2 direction  
3 = material 3 out of plane normal direction  
cf = core failure  
tw = tsai-wu  
[Whole list of symbols](https://ansyshelp.ansys.com/public/account/secured?returnurl=/Views/Secured/corp/v242/en/acp_tut/acp_tut7_postprocess.html)

**IRF** (Inverse reverse factor) is a common indicator used in the composite failure tool to help find out what the critical failure mode is. They allow users to combine and analyze multiple criteria at the same time. It indicates the ratio of stress to material strength. It is the inverse of the safety factor, so an IRF greater than 1.0 signifies that the material has failed or will fail under the given loads. The value is calculated by taking the stress and dividing it by the material's failure stress, with software often using the most conservative value across the material.

Use the **composite sampling point tool** to do detailed failure analysis and figuring out where to apply local reinforcement.

Users can also use **probe** tool in results tab in ANSYS Mechanical to check values at a point or a node.

### Choosing Failure Criteria
**What criteria will you use to determine whether the part passes or fails the load cases?** 
For Example: “The baseplate must withstand all static and dynamic load cases without exceeding a Tsai-Wu failure index of 1 in any ply, with a global displacement under 2 mm, and a minimum factor of safety of 1.5.”

Then improve and try variations.