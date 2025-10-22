# ACP Pre
#note 
ACP PreP: Users can define the individual plies of a composite material by specifying their material, thickness, and orientation within the structure

### Important stuff to set up in ACP

**Materials/Fabrics/Stackups/Sub-Laminates:**
- A Fabric defines the properties of a single layer of material (like fiber and resin) with a specific thickness.
- A Stackup is a predefined combination of fabrics (or a single fabric) with specific ply angles, used for creating common layups. 
- A Sub-laminate is a group of fabrics and stackups that are combined and can be frequently reused in a larger laminate structure

**Element Sets:**
- These are groups of finite elements used for defining the orientation and material properties of composite plies. They act as a scope to define properties like thickness and fiber direction for specific areas of a mesh.

**Rosettes:**
- The X-direction of a rosette determines the in-plane direction of the element lay-up, known as the Oriented Selection Set (OSS) direction, which is crucial for defining how a composite material is placed on a surface, especially for complex 3D geometries.
    
- ACP helps simulate draping effect by having user select between a maximum or minimum angle between the element lay-up and the rosette's Z-direction. This helps pick the most suitable rosette for a specific area, ensuring proper ply orientation and draping for composites.

**OSS (Oriented Selection Set):**
- In simple terms, the real surfaces where layers are applied and set the reference direction for each ply. 

- Oriented Selection Sets in ANSYS ACP are named selections that define a specific orientation for a group of elements, allowing for the creation of complex composite layups where each layer can be oriented differently.

**Selection Rules:**
- Rules are used to define both ply and OSS extends and can be combined with Boolean operations(combine or modify multiple bodies in a geometry). Rules can be re-used as templates and be used to iteratively improve the laminate. (Taking advantage of ACP's ply-based modelling)

**Edge Sets**
- Edge sets are used to define geometric boundaries for applying properties. 

- They are often used to create variable thickness plies along an edge, simulate transitions between different components like scarf joints.

- A tapered edge set in core carbon fiber refers to a manufacturing technique where the material's core—such as foam, honeycomb, or balsa—is machined to gradually reduce in thickness toward the edges. This process creates a smoother transition between the core and the carbon fiber outer layers (skins), which prevents stress concentrations and improves structural performance.

**Modeling Groups:**
- Essentially the actual layup of plies/stackups etc. 
- Make modelling groups in the order of the layup. As a user, you can model as you would build the part. Put ply on ply. And you need not worry about the ply offsets

**Section Cuts:**
- Use Section Cuts to visualize layup geometry

**Geometry**
- Geometries can be used to build complex lay-ups during preprocessing in ACP. For example, core of variable thickness can be modeled as a ply whose thickness is set by an imported geometry of the core. Cut-Off Rules can be based on geometry, therefore controlling the lay-up by a CAD surface or at a pre-defined offset to a CAD surface. Geometries are particularly helpful in generating solid models where geometry-based Extrusion Guides, Snap-To and Cut-Off operations can create intricate shapes.

- CAD geometries are incorporated in an ACP model by creating a link to a **Geometry** in the Workbench Project Schematic or by directly importing an external geometry (IGES or STP format). These CAD geometries may be surfaces, bodies, or assemblies of parts. The concept of virtual geometries allows you to select and group specific regions or bodies of the imported CAD geometry and use them for subsequent modeling operations. All geometry-based operations are based on virtual geometries. Virtual geometries act as a reference to one of more faces or bodies of one CAD geometry.

For more info: https://ansyshelp.ansys.com/public/account/secured?returnurl=/Views/Secured/corp/v242/en/acp_ug/acp_CAD_Geometries.html


**Solid Models**
- In ANSYS ACP (Composite PrepPost), solid models represent the full, 3D volume of a composite part, and they can be generated in two main ways: Solid Model (by extruding a 2D shell mesh) or as an [Imported Solid Model](https://www.google.com/search?sca_esv=d9aed0d2e07b8d48&cs=0&q=Imported+Solid+Model&sa=X&ved=2ahUKEwirlP_9tK6QAxU1EFkFHS3jGlQQxccNegQIAhAC&mstk=AUtExfDTJ2LwIdQzvrFAZBhCIwykvvj8iORvaHh82l0HOXimufiGP04jGL5c3YpP4TJCfNm-sOs9gRcqq-QJq7hFhGKICr5gcwkujaojO4OGRi698asCd4GDw2C87LK9rlU8IknGSNH6dDgz7W0kcav3sm9oCG8zs8BJqDxsGWzwYipExL7mHeFqL3ov4VsiCXALp6CFKSBqrYT_6V0CkFP6F-yHYw&csui=3) (by loading a pre-existing 3D mesh from an external source). 