# 🌎 React Globe

Create beautiful and interactive React + ThreeJS globe visualizations with ease.

![image](https://raw.githubusercontent.com/chrisrzhou/react-globe/master/cover.png)

## Features

- ✨ Beautiful and complete with clouds, backgrounds and lighting.
- ✌️ Incredibly simple to use and configure.
- 🤸‍ Easy globe animations.
- 📍 Render interactive markers on the globe with simple data.
- ⚛️ Modern Javascript + build tools.

## Install

```bash
yarn add react-globe
```

Note that `react-globe` requires `react >= 16.8.0` and `three >= 0.102.0` as peer dependencies.

## Examples

### Documented Examples

View all documented examples at https://react-globe.netlify.com/

### Local Examples

You can also run the examples locally:

```bash
git clone git@github.com:chrisrzhou/react-globe

cd react-globe
yarn
yarn dev
```

### Simple Example (no props)

<iframe src="https://codesandbox.io/embed/88645px230?fontsize=14" title="react-globe-simple" style="width:100%; height:500px; border:0; border-radius: 4px; overflow:hidden;" sandbox="allow-modals allow-forms allow-popups allow-scripts allow-same-origin"></iframe>

Here is a simple example with no props!

### Interactive Example (with markers)

<iframe src="https://codesandbox.io/embed/p5lwvkp7x?fontsize=14" title="react-globe-interactive" style="width:100%; height:500px; border:0; border-radius: 4px; overflow:hidden;" sandbox="allow-modals allow-forms allow-popups allow-scripts allow-same-origin"></iframe>

## Development

### Main Dependencies

- `react`
- `three`
- `three-orbitcontrols`
- `three.interaction`
- `es6-tween`
- `tippy.js`

### Codebase Overview

- `ReactGlobe.tsx`: Core component that combines React + ThreeJS hooks into an animated scene supporting interactions.
- `Tooltip.tsx`: Tooltip component powered by `tippy.js`.
- `reducer.ts`: Simple state management for tracking focused coordinates and active markers.
- `defaults.ts`: Default options and constants.
- `utils.ts`: Various simple functions to compute derived data.
- `/hooks`: React hooks to handle updating various ThreeJS entities (e.g. camera, globe, markers, renderer).
- `/textures`: Default globe, clouds and background textures.

The code is written in `typescript`, linted with `eslint` + `prettier`, and built with `rollup`. Examples and documentations are built with `docz`.

## Areas of Improvements

These are some areas of improvements for `react-globe`. PRs and help is greatly appreciated!

- [ ] Various dependencies are untyped. I am also fairly new to Typescript so PRs to improve type quality in the codebase is appreciated :)
- [ ] Check that React hooks are decoupled, bugfree and performant.
- [ ] Surface various hardcoded constants in `default.ts` as prop options. We need to be mindful about keeping the component props API simple and easy to use.
- [ ] Support more marker types e.g. `path`, `area`
- [ ] Provide better ways to render custom globes and markers. We might want to avoid overcomplicating the component, and this could be moved into another package.
- [ ] Provide better ways to 'script' animations vs the current simple approach of using an array of `Animation`. `react-spring`'s animation scripting is a good approach to do this.

## Donate

My projects will always be (ads-)free. I constantly learn from the community, so these projects are a way of giving back to the community. If you liked this project or find it useful, feel free to buy me a cup of coffee ☕️ through a small donation!

[![paypal](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.me/chrisrzhou/5)