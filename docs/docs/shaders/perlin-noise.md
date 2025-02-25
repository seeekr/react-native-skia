---
id: perlin-noise
title: Perlin Noise Shaders
sidebar_label: Perlin Noise
slug: /shaders/perlin-noise
---


## Fractal Perlin Noise Shader

Returns a shader with Perlin Fractal Noise.

| Name        | Type           |  Description                    |
|:------------|:---------------|:--------------------------------|
| freqX       | `number` | base frequency in the X direction; range [0.0, 1.0]|
| freqY       | `number` | base frequency in the Y direction; range [0.0, 1.0] |
| octaves     | `number`         |  |
| seed        | `number`     | |
| tileWidth?  | `number`     | if this and `tileHeight` are non-zero, the frequencies will be modified so that the noise will be tileable for the given size. |
| tileHeigth? | `number`       | if this and `tileWidth` are non-zero, the frequencies will be modified so that the noise will be tileable for the given size. |

### Example
```tsx twoslash
import React from "react";
import {
  Canvas,
  Paint,
  Rect,
  FractalNoise,
  Skia,
  Shader,
  Fill,
  vec
} from "@shopify/react-native-skia";

export const FractalNoiseDemo = () => {
  return (
    <Canvas style={{ flex: 1 }}>
      <Paint>
        <FractalNoise freqX={0.05} freqY={0.05} octaves={4} />
      </Paint>
      <Fill color="white" />
      <Rect x={0} y={0} width={256} height={256} />
    </Canvas>
  );
};
```
### Result
![Fractal](assets/fractal.png)

## Turbulence Perlin Noise Shader

Returns a shader with Perlin Turbulence.

| Name        | Type           |  Description                    |
|:------------|:---------------|:--------------------------------|
| freqX       | `number` | base frequency in the X direction; range [0.0, 1.0]|
| freqY       | `number` | base frequency in the Y direction; range [0.0, 1.0] |
| octaves     | `number`         |  |
| seed        | `number`     | |
| tileWidth?  | `number`     | if this and `tileHeight` are non-zero, the frequencies will be modified so that the noise will be tileable for the given size. |
| tileHeigth? | `number`       | if this and `tileWidth` are non-zero, the frequencies will be modified so that the noise will be tileable for the given size. |

### Example
```tsx twoslash
import React from "react";
import {
  Canvas,
  Paint,
  Rect,
  Turbulence,
  Skia,
  Shader,
  Fill,
  vec
} from "@shopify/react-native-skia";

export const TurbulenceDemo = () => {
  return (
    <Canvas style={{ flex: 1 }}>
      <Paint>
        <Turbulence freqX={0.05} freqY={0.05} octaves={4} />
      </Paint>
      <Fill color="white" />
      <Rect x={0} y={0} width={256} height={256} />
    </Canvas>
  );
};
```
### Result
![Turbulence](assets/turbulence.png)
