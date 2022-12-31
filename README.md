# Maya-Mel-Scripts
A Collection of Very Old MEL Scripts That You May Find Useful

# daConverMelToCPP 1.4
This procedure converts a mel file into a const char variable to be used within a cpp project. If you are writing a Maya plugin and don't want to deal with a stack of MEL files, it can be neater to include the MEL scripts in your plugin.

# daPanAndScanTool
This obsolete tool will allow the user to interactively track and zoom the current camera's image plane by clicking and dragging in the workspace. It can be used to model accurately from photographic references using a camera that matches the focal length and film back settings of the camera used to capture the image. This functionality is now implemented in Autodesk Maya.

# da_AlignMoveToolToCamera
This proc aligns the move tool's Z axis to the current camera's angle of view. It is useful for matching geometry to 3d tracked footage. Simply select a point and run script. If anyone wants an explainer video just drop me a line in the contact section.

# da_apply_delta
This simple proc will compare two meshes: a base mesh and a deformed mesh. It then calculates the vert deltas and applies it to the third mesh.

# da_fleshyEyeWidget_v2
This procedure creates a fleshy eye widget that controls the blendshape targets associated with the eyeball. ( There are better ways of rigging a fleshy eye :D )
        
# da_instanceGeometryV3
This was written when computers did not have half the memory they do now. This proc converts geometry into instances for use in dynamic simulations. If you model a fractured object the proc will create a particle object whos particles are placed within the geometry objects and an instancer node that replaces the geometry with instances. The original geometry will be hidden. Then it is easier to simulate ¯\_(ツ)_/¯
        
# da_matchComponentsPosV2
This simple proc will match the position of corresponding components. First: shift select all straying cv's on deformed surface. Second: shift select the target shape. Third: argument: 0 matches world space position, 1 matches local position. Fourth: run proc.
        
# da_moveFollicle
This script will move a follicle to a specific UV parameter value. Select the follicle and a surface point on nurbs surface, Run the script and the follicle will jump to desired position.
        
# da_replaceObject
This simple proc will replace one object with another. Its useful when assembling a scene.

# da_snapToSurfaceV3
This script will snap a cv or vertex to the closest point on a nurbs surface.
