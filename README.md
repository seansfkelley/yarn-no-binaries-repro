# yarn-no-binaries-repro

To reproduce:

```
yarn install
cd packages/b
yarn webpack
```

Note that it complains that there is no Webpack available.

To resolve the issue, do any single one of the following:

- remove `webpack` dependency from `a`
- remove `hoistingLimits` configurtion from `a`
- remove `@storybook/react` dependency from `b`

Then `yarn install` and try `yarn webpack` from `b`.
