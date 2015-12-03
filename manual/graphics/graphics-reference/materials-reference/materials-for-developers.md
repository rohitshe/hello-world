# Materials For Developers

The following diagram shows the Material interfaces and implementation classes:

- The interface `IMaterialDescriptor (ref:{SiliconStudio.Xenko.Rendering.Materials.IMaterialDescriptor})` is the root interface for a material description.
- The `IMaterialShaderGenerator (ref:{SiliconStudio.Xenko.Rendering.Materials.IMaterialShaderGenerator})` is the main interface used to generate a material shader of the material.
- Each attributes and layers are implementing this interface to modify the final material shader.
- The `MaterialDescriptor (ref:{SiliconStudio.Xenko.Rendering.Materials.MaterialDescriptor})` is the editor-time description of the material before being compiled into a Material Shader.
- The `Material (ref:{SiliconStudio.Xenko.Rendering.Material})` class is the runtime material shader generated from the `MaterialDescriptor (ref:{SiliconStudio.Xenko.Rendering.Materials.MaterialDescriptor})`

![images/materials-for-developers-1.png](images/materials-for-developers-1.png) 

 

