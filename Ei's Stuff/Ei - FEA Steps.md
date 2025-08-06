1. Open Workbench
    
2. Select Static Structural 
    
3. Select Materials in Engineering Data 
    
4. Import Geometry by importing a CAD (STEP File)
    
5. export step file from cad software 
    
6. Right click on model and click edit
    
7. Generate Mesh 
    
8. Check mesh quality 
    
9. If there are weird alignments changed mesh method (to a different shape)
    
10. If quality is still bad (i.e., a lot of red spots reduce mesh size)
    
11. Then define fixed supports (see which side doesn’t move i.e., if it’s a box and the force is applied from above the bottom doesn’t move)
    
12. Then apply force (choose the direction of force, choose magnitude of force, choose which face to apply the force to)
    
13. Confirm with Hand Calculations
  

### Hand Calculations for Stress and Strain

  

### Multiaxial Hooke's Law
$\sigma_1=\frac{E}{1-\nu^2}(\varepsilon_1+\nu\cdot\varepsilon_2)$
$\sigma_2=\frac{E}{1-\nu^2}(\varepsilon_2+\nu\cdot\varepsilon_1)$

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcRs_lQyaoXzKxEzRXDMNlbndrrcgRcbveLqDWNnnBjVRW7XBSOeYnMCQUSZnYjehI6ucSiDMHpqBNVCMAE8c-EvyeETTW-_etIx71PZTvYgFNV-M6uykNeSc9rOFqi9VWsBxL-ig?key=gpXBfoP2HieI4HeUEA6Y-Cji)

  
$\varepsilon_x=\frac{1}{E}(\sigma_x-\nu(\sigma_y+\sigma_z))$
$\varepsilon_y=\frac{1}{E}(\sigma_y-\nu(\sigma_x+\sigma_z))$
$\varepsilon_z=\frac{1}{E}(\sigma_z-\nu(\sigma_x+\sigma_y))$


$\nu=$ Poisson’s ratio (different for each material)

$\sigma=\text{stress}=\frac{F}{A}$


