#### Introduce

- Here we take some examples to explan the differences between `esbuild`, `babel`, `webpack` and `babel + webpack`.

#### Testing

```
/* NOTE: polyfill entire without optimization will make file larger more
         TEST: toggle off the import below
 */
import 'core-js/stable';

to

/* NOTE: polyfill entire without optimization will make file larger more
         TEST: toggle off the import below
 */
// import 'core-js/stable';
```

```
yarn build
yarn build:esnext
yarn build:babel  // Normally, the output can not run on browser environment. (ex: import syntax -> require syntax)
yarn build:babel-webpack
```

### Purpose between babel and webpack

- Babel: make import to require and some of new syntax and API transform.
- (*)Webpack make required 3rd party lib to inline source of output file.

- `Esbuild` ~= `webpack` + `babel` without polyfill(ex: `core-js`)
  - Esbuild also provide some of newer API downgrade transform. ex: Async/Await to Promise.
