# ACP
#topic 

Author: [[yohanne|Yohanne]]

### Very Basic ACP Workflow
1. Open Workbench
    
2.  Check and plan layup information 
    
3. Select ACP and import geometry of layup mold using CAD file
    
4. Edit Engineering Data in ACP and select from engineering material library or add your own
    
5. Define material behavior
    
6. Right click on model and click edit
    
7. Generate mesh (Remember to specify a dummy thickness and material for mold)
    
8. Check mesh quality 
    
9. ACP setup fabrics/stackups if needed
    
10. Check element sets. Create rosette and OSS (model as you build it )
    
11. Create plies to make modeling group (use section cuts to see if layup looks normal)
    
12. import geometry if there is solid modeling or varying thickness
    
13. Add static structural and start post analysis (add boundary conditions and loads first rest is similar to FEA)

### Features
- Ply-based approach 
- Advanced Analysis that supports the analysis of **residual stress** and perform iterations to find first failing ply
- Find ultimate failure (doesn't stop at first crack)
- Scripting (using python)
- **Useful because you can model as you build --> makes using ACP very intuitive**

### Subtopics
[[ACP Pre-Processing]]
[[ACP Mechanical Modeling]]
[[ACP Theory]]
[[ACP Post-Processing]]
