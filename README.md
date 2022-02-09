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
```
