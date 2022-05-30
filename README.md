# repro-jest28-uuid

Reproducing an issue encountered while bumping from Jest 27 to Jest 28 with JSDom enabled.

Jest tries to import the browser version of the package uuid, as soon as we toggle jsdom mode. This version comes with two issues:

- ESM only: _we can bypass it by transpiling it to commonjs via babel_
- Use internals specific to browsers and not available in node
