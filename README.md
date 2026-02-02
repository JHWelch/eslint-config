# @jhwelch/eslint-config

This is a shared ESLint config for JHWelch projects.

It currently supports a TypeScript project with Vue.

## Installation

```bash
npm install --save-dev eslint @jhwelch/eslint-config
```

## Usage

The simplest usage without any modification 

```mjs
// eslint.config.mjs
import { defineConfig } from 'eslint/config';
import jhwelch from '@jhwelch/eslint-config'

export default defineConfig([
  ...jhwelch,
])
```

You can override the rules by extending the config. See the [ESLint Documentation](https://eslint.org/docs/latest/extend/shareable-configs#overriding-settings-from-shareable-configs) for more information.

```mjs
// eslint.config.mjs
import { defineConfig } from 'eslint/config';
import jhwelch from '@jhwelch/eslint-config'

export default defineConfig([
  ...jhwelch,
  {
    rules: {
      'no-unused-vars': 'warn',
    },
  },
])
```
