# omniscient webpack hot reload loader

`omniscient-hot-reload-loader` is a webpack loader for [omniscient components](https://github.com/omniscientjs/omniscient) that lets you have hot reloading components in your development environment, i.e. components who will re-render automatically when they are changed, without a page refresh.

## How it works
By substituting calls to `component('SomeComponent', function() { ... )` with code utilizing webpacks [hot module replacement](https://github.com/webpack/docs/wiki/hot-module-replacement-with-webpack), it is possible to detect changes to a component, and patch the prototype of matching components that are already rendered with the methods of the changed component. By subsequently forcing re-render, components will automatically re-render when changed, while state will be kept in tact.

This is exactly how [react-hot-loader](https://github.com/gaearon/react-hot-loader), for normal React classes, adapted to work with omniscient.
