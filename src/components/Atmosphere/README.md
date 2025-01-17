---
description: Atmosphere Layer Component
---

# Atmosphere

## Props

<table><thead><tr><th width="194">Name</th><th width="135.33333333333331">Type</th><th>Description</th></tr></thead><tbody><tr><td>style</td><td>object</td><td><a href="https://docs.mapbox.com/mapbox-gl-js/style-spec/fog/">Fog style specs</a></td></tr></tbody></table>

_\*required_

## Example

```jsx
import { Component, createSignal } from "solid-js";
import MapGL, { Viewport, Atmosphere } from "solid-map-gl";
import 'mapbox-gl/dist/mapbox-gl.css';

const App: Component = () => {
  const [viewport, setViewport] = createSignal({
    center: [0, 52],
    zoom: 6,
    pitch: 100
  } as Viewport);

  return (
    <MapGL
      options={{ style: 'mb:sat_street' }}
      viewport={viewport()}
      onViewportChange={(evt: Viewport) => setViewport(evt)}
    >
      <Atmosphere />
    </MapGL>
  );
};
```
