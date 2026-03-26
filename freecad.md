# FreeCAD

## FEM

If you get "nonpositive jacobian determinant" in trying to run CalculiX, go back to Gmsh or whatever and try setting a "maximum size".
When you calculate the mesh with Gmsh if it gives you some warnings this seems to correlate with "nonpositive jacobian determinant". Just
mess about with Gmsh until it doesn't generate warnings and then try CalculiX again.
