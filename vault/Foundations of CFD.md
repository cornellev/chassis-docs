# Foundations of CFD
#note

## The Black Box
### What's inside the Black Box?

The User Inputs go into a **Mathematical Model** (based on the [[Navier Stokes Equations]]), which solve a large system of equations to compute the *primary unknowns at selected points.* Remember: This has to be done in conjunction with hand calculations and experimental data, otherwise we have "garbage in, garbage out" - meaning that we wont know whether our data makes physical sense or not without having an expectation going in.
### Verification and Validation
**Verification**: Did I solve the model right?
- Check consistency with mathematical model, level of numerical errors, comparison with hand calculations
**Validation**: Did I solve the right model?
- Check against experimental data

### CFD Problem Solving Framework
See the [PDF here](https://ecornell.s3.amazonaws.com/content/MAE/MAE111/mae111_tool-framework.pdf) for a more graphical intuition of what's going on.

*This framework can be used to solve CFD problems, allowing you to focus on observable actions such as inputs and outputs. Below are the steps of this approach.*

**Problem Specification**
1. Pre-analysis
2. Geometry
3. Mesh
4. Mathematical Model Setup
5. Numerical Solution
6. Post-Processing
7. Verification and Validation


**NOTE**: There's a course project at the bottom, but in my (Lucas') opinion, I don't really think that it's that helpful. Especially if you've done ANSYS before, I think as long as you carry that mindset into CFD you should be fine.
