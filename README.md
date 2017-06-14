## aframe-follow-spline-component

Make A-Frame entity follow a spline curve path.

![A-Frame follow spline component](https://raw.githubusercontent.com/caseyyee/aframe-follow-spline-component/master/images/preview.gif)

This component implements three.js  [CatmullRomCurve3](https://threejs.org/docs/#api/extras/curves/CatmullRomCurve3)
For [A-Frame](https://aframe.io).

### Usage

```html
<head>
  <title>My A-Frame Scene</title>
  <script src="https://aframe.io/releases/0.5.0/aframe.min.js"></script>

  <!-- Include component script into your project along with A-Frame. -->
  <script src="https://unpkg.com/aframe-follow-spline-component/dist/aframe-follow-spline-component.min.js"></script>
</head>

<body>
  <a-scene>
    <!-- Add component to entity -->
    <a-entity follow-spline></a-entity>
  </a-scene>
</body>
```

### Component options

| Property | Description | Default Value |
| -------- | ----------- | ------------- |
| preset | Predefined path to follow.  Look for all the preset options below | orbit |
| points | Array of points along the curve. | None |
| time | number of seconds to complete a circuit of the line | 10 | 
| alignWithPath | Align entity in the direction of travel on path | false |
| showpath | Display the path which entity will follow. | false |
| closed | Loop path back onto self. | false |
| type | Sets curve type. See below for all curve types. | centripetal |
| tension | When type is catmullrom, defines catmullrom's tension. | 0.5 |

### Defining custom path.
You can specify a custom curve by using the `points` option to define a array of points for the entity to follow.

```html
<a-entity follow-spline="points: -2 1 0, 0 1 -3, 2 5 -3, 2 1 3, -3 1 3, -2 1 0;"></a-entity>
```
#### Curve Types
To be added.

### Built-in Presets

#### Orbit
Orbits camera around the entity.


### Combine with other components

#### Attached to `camera` and using `look-at` will orbit the camera around the entity.

```html
<a-box id="target"></a-box>
<a-entity camera follow-spline look-at="#target"></a-entity>
```

#### npm

Install via npm:

```bash
npm install aframe-follow-spline-component
```

Then require and use.

```js
require('aframe');
require('aframe-follow-spline-component');
```
