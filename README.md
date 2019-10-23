Demonstration of a bug in NPM which patches "package.json" of every
installed package with asbolute path to it.

how to test:

1. clone repository
2. run `npm install`
3. then run `fgrep -Rn '_where' node_modules/*`
4. observe `package.json` of `lodash` to have absolute path to curent
   folder

   ```
   $ fgrep -Rn "_where" node_modules/*

    node_modules/lodash/package.json:25:  "_where": "......",
   ```
