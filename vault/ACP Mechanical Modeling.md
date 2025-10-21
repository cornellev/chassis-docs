# Setting up the Model
#note 

- Create Named selections and remote points if needed 
- Generate Mesh if needed 
- Add boundary conditions and loads in static structural
- Find solution 

### Some useful tools 
- A deformable remote point allows applied loads or constraints to act on a surface while permitting that surface to deform freely without adding stiffness to the model. This is useful for representing a boundary that is less stiff than the main part or when you want to apply an average force or displacement to a complex geometry without stiffening it, such as a flexible connection or a thermal expansion scenario. 

  A remote displacement is a boundary condition that applies constraints to a geometric face or volume via a central "remote point". It is used to define complex motions and rotations for large or difficult-to-mesh parts, simplifying simulations by linking the nodes on the surface to a single point with six degrees of freedom (three translations and three rotations). This allows for a more realistic and controllable application of loads and constraints than applying them directly to every node on a surface.

- 
