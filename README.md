# @tysian/eslint-config-monorepo

ESLint config.

Based on:

- [StandardJS config](https://github.com/standard/eslint-config-standard)
- [Airbnb config](https://github.com/airbnb/javascript)
- [Antfu config](https://github.com/antfu/eslint-config)

Monorepo setup inspired by [Anthony Fu](https://github.com/antfu).

## Install

```bash
npm install eslint @tysian/eslint-config --save-dev
```

### Install with typescript

> **Note** Base config included

```bash
npm install eslint @tysian/eslint-config-typescript --save-dev
```

### TypeScript Aware Rules

Type aware rules are enabled when a tsconfig.eslint.json is found in the project root, which will introduce some stricter rules into your project. If you want to enable it while have no tsconfig.eslint.json in the project root, you can change tsconfig name by modifying ESLINT_TSCONFIG env.

```js
// .eslintrc.js
process.env.ESLINT_TSCONFIG = 'tsconfig.json';

module.exports = {
  extends: '@tysian/eslint-config-typescript',
};
```

### Install with React

> **Note** Base & typescript configs included

```bash
npm install eslint @tysian/eslint-config-react --save-dev
```

> **Note** `.eslintignore` already provided in config

### Prettier

Recommended to use along with [prettier](https://github.com/prettier/prettier):

```bash
npm install prettier eslint-config-prettier --save-dev
```

## Config `.eslintrc`

```json
{
  "extends": [
    "@tysian",
    // your other configs
    "prettier"
  ]
}
```

### Without prettier

```json
{
  "extends": ["@tysian"]
}
```

_Cheese_ 🧀
