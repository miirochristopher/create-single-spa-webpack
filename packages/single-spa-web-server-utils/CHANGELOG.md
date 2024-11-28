# single-spa-web-server-utils

## 2.3.2

### Patch Changes

- [#393](https://github.com/single-spa/create-single-spa/pull/393) [`181da9a`](https://github.com/single-spa/create-single-spa/commit/181da9a5aecd7a9b8fc99dbb965d106d7b74b3de) Thanks [@ibacher](https://github.com/ibacher)! - Bump dependency versions to compatible versions without vulnerabilities

## 2.3.1

### Patch Changes

- [#348](https://github.com/single-spa/create-single-spa/pull/348) [`8caae1c`](https://github.com/single-spa/create-single-spa/commit/8caae1cb2f3df5cc2bfcb185dc10da141f21756d) Thanks [@joeldenning](https://github.com/joeldenning)! - Fix bad publish - new functions are now exposed properly in API

## 2.3.0

### Minor Changes

- [#347](https://github.com/single-spa/create-single-spa/pull/347) [`98a6e0a`](https://github.com/single-spa/create-single-spa/commit/98a6e0a9ae52b3bda1dddae121098a88523207c7) Thanks [@joeldenning](https://github.com/joeldenning)! - Add new clearAllIntervals and reset functions

### Patch Changes

- [#347](https://github.com/single-spa/create-single-spa/pull/347) [`98a6e0a`](https://github.com/single-spa/create-single-spa/commit/98a6e0a9ae52b3bda1dddae121098a88523207c7) Thanks [@joeldenning](https://github.com/joeldenning)! - Catch all promises in getImportMaps, to avoid unhandled rejections

## 2.2.0

### Minor Changes

- [#327](https://github.com/single-spa/create-single-spa/pull/327) [`5c31d36`](https://github.com/single-spa/create-single-spa/commit/5c31d3639e8663be97e435366615f7553341d453) Thanks [@joeldenning](https://github.com/joeldenning)! - Update all dependencies

## 2.1.1

### Patch Changes

- [#300](https://github.com/single-spa/create-single-spa/pull/300) [`0ca13bb`](https://github.com/single-spa/create-single-spa/commit/0ca13bb8de64b2329bae04f7bf92b1e9fcb5c47a) Thanks [@joeldenning](https://github.com/joeldenning)! - Breaking Changes

  - NodeJS >= 12.13.0 now required, as we're using [style-loader@3](https://github.com/webpack-contrib/style-loader/releases/tag/v3.0.0) in webpack-config-single-spa

  Projects generated by single-spa

  - New projects use Jest 27 (https://jestjs.io/blog/2021/05/25/jest-27#miscellaneous-breaking-changes), including jest-util and babel-jest
  - Newly generated projects use React 17 types
  - Newly generated projects now use concurrently 6. See https://github.com/kimmobrunfeldt/concurrently/releases/tag/v6.0.0
  - Newly generated root configs and util modules now execute `git init` during creation
  - Newly generated projects now use eslint-config-prettier 8. See https://github.com/prettier/eslint-config-prettier/blob/main/CHANGELOG.md#version-800-2021-02-21

  Internal changes

  - Upgrade yargs to 17 in create-single-spa, which parses the CLI args. See https://github.com/yargs/yargs/releases/tag/v17.0.0
  - Upgrade yeoman-environment to v3 and yeoman-generator to v5. This comes with changes to how packages are installed by yeoman, but those changes don't apply to create-single-spa because only committed package.jsons result in yeoman-environment installs. Manually installing dependencies the old way via yeoman-generator.

  Maintenance

  - Upgrade to jest 27 (https://jestjs.io/blog/2021/05/25/jest-27#miscellaneous-breaking-changes), including jest-util and babel-jest
  - Upgrade create-single-spa to husky 6. Upgrade newly generated projects to use husky 6
  - Add `scripts/update-dependencies.sh` script for maintainers to easily upgrade all dependencies at once

## 2.1.0

### Minor Changes

- 905c0cc: - The create-single-spa project now uses pnpm workspaces and changesets instead of lerna.
  - Remove deprecated babel-eslint package in favor of new @babel/eslint-parser package.
  - Fix typescript problems in pnpm packages.
  - Add support for creation of pnpm packages. Resolves #211.
  - Add name field for utility packages.
  - No longer depend on beta versions of create-single-spa packages
  - Rename template package.jsons to avoid detection by monorepo tooling
  - Fix usage of @testing-library/jest-dom in yarn pnp and pnpm
  - Switch to Github actions instead of Travis - travis stopped reporting test results
  - prettierignore pnpm-lock.yaml files
  - Improve support for format and check-format commands on Windows