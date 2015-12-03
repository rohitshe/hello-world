# Custom Scene Renderer

You can create custom renderer by implementing directly the `ISceneRenderer (ref:{SiliconStudio.Xenko.Rendering.ISceneRenderer})` or by using a delegate through the `SceneDelegateRenderer (ref:{SiliconStudio.Xenko.Rendering.SceneDelegateRenderer})`

# Implementing an ISceneRenderer

You can use a base implementation of this interface

- `SceneRendererBase (ref:{SiliconStudio.Xenko.Rendering.SceneRendererBase})`: Provides a default implementation of `ISceneRenderer (ref:{SiliconStudio.Xenko.Rendering.ISceneRenderer})` and automatically binds the output defines on the renderer to the GraphicsDevice before calling the `DrawCore` method.
- `SceneRendererViewportBase (ref:{SiliconStudio.Xenko.Rendering.SceneRendererViewportBase})`: Inherits from `SceneRendererBase (ref:{SiliconStudio.Xenko.Rendering.SceneRendererBase})` and add the ability to configure a specific viewport 

 

```cs
[DataContract("MyCustomRenderer")]
[Display("My Custom Renderer")]
public sealed class MyCustomRenderer : SceneRendererBase
{
    // Implements the DrawCore method
    protected override void DrawCore(RenderContext context, RenderFrame output)
    {
        // Access to the graphics device
        var graphicsDevice = context.GraphicsDevice;
        // Clears the the currrent render target
        graphicsDevice.Clear(output.RenderTargets[0], Color.CornflowerBlue);
        // [...] 
    }
}```


# Using a delegate

In some scenarios, you simply want to develop a renderer and attach it to a method directly. You can use a `SceneDelegateRenderer (ref:{SiliconStudio.Xenko.Rendering.SceneDelegateRenderer})` for this usage:

```cs
var sceneDelegateRenderer = new SceneDelegateRenderer(
    (renderContext, frame) =>
    {
        // Access to the graphics device
        var graphicsDevice = context.GraphicsDevice;
        // Clears the the currrent render target
        graphicsDevice.Clear(output.RenderTargets[0], Color.CornflowerBlue);
        // [...] 
   });```


