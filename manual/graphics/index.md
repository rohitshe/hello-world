# Graphics

# Shaders

**[Shaders](graphics-reference/effects-and-shaders-reference/shading-language/index.md)** in Xenko are extended shaders derived from `HLSL`.

They provide true **composition** of modular shaders through the use of **[inheritance](graphics-reference/effects-and-shaders-reference/shading-language/classes-mixins-and-inheritance.md)**, shader **[mixins](graphics-reference/effects-and-shaders-reference/shading-language/composition.md)** and **[automatic weaving of shader in-out attributes](graphics-reference/effects-and-shaders-reference/shading-language/automatic-shader-stage-input-output.md)**.

# Effects

**[Effects](graphics-reference/effects-and-shaders-reference/effect-system/index.md)** in Xenko combines shaders into a full shader. They provide conditional **[composition](graphics-reference/effects-and-shaders-reference/effect-system/effect-language.md)** of shaders and **[effect permutations](graphics-reference/effects-and-shaders-reference/effect-system/effect-permutations.md).**

# Target everything

Xenko shaders are converted automatically to the target graphics platform, either plain HLSL or GLSL output shader files.

For mobile platforms, shaders are optimized by a GLSL optimizer in order to improve performance on these devices.

# Advanced Graphics

The Graphics module provides a set of comprehensive methods to display the game. Although the engine is available on multiple platforms, the whole system behaves like DirectX 11 from the user perspective.

A basic prior knowledge of the rendering pipeline is expected from the user.

## Topics

- [Graphics Device Reference](graphics-reference/graphics-device-reference/index.md)
- [Render states](graphics-reference/graphics-device-reference/render-states.md)
- [Textures and render targets](graphics-reference/graphics-device-reference/textures-and-render-targets.md)
- [Displaying a texture](graphics-reference/graphics-device-reference/draw-a-texture.md) on an off screen
- [Draw vertices](graphics-reference/graphics-device-reference/draw-vertices.md)
- Displaying multiple sprites: [SpriteBatch](graphics-reference/graphics-device-reference/spritebatch.md)
- Displaying text: [SpriteFont](graphics-reference/graphics-device-reference/spritefont.md)
- Using [shaders and effects](graphics-reference/effects-and-shaders-reference/index.md)

