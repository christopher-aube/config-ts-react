# Config TS React

This repo is intended to provide basic configuration for [react](https://reactjs.org/) [typescript](https://www.typescriptlang.org/) projects.

It also includes configurations for [ESLint](https://eslint.org/), [style lint](https://stylelint.io/), and [prettier](https://prettier.io/).

## Adding as a dependency

You can add this as a dependency by including the following in your `package.json` dependency list.

```
"config-ts-react": "git+https://git@github.com/christopher-aube/config-ts-react.git",
```

If you want to use a specific release use the follow instead:

> <br />
> Replace "v0.0.1" with the specific release tag that you want to use.
>
> <br />

```
"config-ts-react": "git+https://git@github.com/christopher-aube/config-ts-react.git#v0.0.1",
```

## Usage

In your `package.json` add the following at the root level:

```json
  "eslintConfig": {
    "extends": "config-ts-react"
  },
  "prettier": "config-ts-react/prettier",
  "stylelint": {
    "extends": "config-ts-react/stylelint"
  }
```

Then in your `tsconfig.json` add the following at the root level:

```json
{
  "extends": "config-ts-react/tsconfig",
  "compilerOptions": {
    "types": ["config-ts-react/src/typings"]
  }
}
```