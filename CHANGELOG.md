# Changelog

All notable changes to this project will be documented in this file. See [standard-version](https://github.com/conventional-changelog/standard-version) for commit guidelines.

## 2.3.0 (2024-04-01)


### Features

* add option to set global defaults ([95cf340](https://github.com/Paladin-Analytics/mongoose-lean-defaults/commit/95cf34032370d180a8774e653086e1873097a8ee)), closes [#28](https://github.com/Paladin-Analytics/mongoose-lean-defaults/issues/28)
* respect projection ([f0affd4](https://github.com/Paladin-Analytics/mongoose-lean-defaults/commit/f0affd4df8df4a163659731c8cec703448c578f8))


### Bug Fixes

* 🏷️ make sure types work with typed Schema ([2987e41](https://github.com/Paladin-Analytics/mongoose-lean-defaults/commit/2987e4135bde915db1b077e8f1d8a80d00aaf464))
* don't apply plugin logic if lean is not used ([5fccc25](https://github.com/Paladin-Analytics/mongoose-lean-defaults/commit/5fccc2563c8e450d3404306cec78edb8eeea2f18)), closes [#29](https://github.com/Paladin-Analytics/mongoose-lean-defaults/issues/29)
* handle `$slice` and `$elemMatch` projections ([e30fdc4](https://github.com/Paladin-Analytics/mongoose-lean-defaults/commit/e30fdc4e9b2962289727ef993f194f6ac1da09a4)), closes [Automattic/mongoose#9149](https://github.com/Automattic/mongoose/issues/9149)
* make it work with other lean libraries ([82765be](https://github.com/Paladin-Analytics/mongoose-lean-defaults/commit/82765befcc27f67ec270c689137803b16fe468d1))
* **nested objects:** old null values were breaking nested defaults ([9f05cb1](https://github.com/Paladin-Analytics/mongoose-lean-defaults/commit/9f05cb1a3d6bd94c95da38588012d3c514f08aa5))
* respect default undefined value for subschemas ([2cc0fe2](https://github.com/Paladin-Analytics/mongoose-lean-defaults/commit/2cc0fe298e623fc3053b6aa81113368765f071dd)), closes [#30](https://github.com/Paladin-Analytics/mongoose-lean-defaults/issues/30)
* support mongoose 5 ([8a748ab](https://github.com/Paladin-Analytics/mongoose-lean-defaults/commit/8a748ab9354faac0ebf99d715c985c74236a1056))

# 2.2.1 / 2022-06-24

- Fixed: Respect default value of `undefined` for subschemas [#30](https://github.com/DouglasGabr/mongoose-lean-defaults/issues/30)
- Fixed: Do not run plugin logic if not using `.lean()` [#29](https://github.com/DouglasGabr/mongoose-lean-defaults/issues/29)

# 2.2.0 / 2022-06-17

- Added: Option to provide global defaults when attaching plugin to schema [#28](https://github.com/DouglasGabr/mongoose-lean-defaults/issues/28)

# 2.1.2 / 2022-06-17

- Fixed: Support mongoose 5 [#27](https://github.com/DouglasGabr/mongoose-lean-defaults/issues/27)

# 2.1.1 / 2022-06-03

- Fixed: Make it work reliably with other `lean` plugins
- Refactored: Code refactored so it is simpler to maintain

# 2.1.0 / 2022-02-08

- Fixed: Fields using Map type receive an additional "$\*" key in the result [#24](https://github.com/DouglasGabr/mongoose-lean-defaults/issues/24)
- Fixed: Recursive schema on array field causes stack overflow [#25](https://github.com/DouglasGabr/mongoose-lean-defaults/issues/25)
- Added: Attach plugin to `findOneAndRemove` and `findOneAndDelete`
- Added: Support mongoose v6 (`>=5` in `peerDependencies`)

# 2.0.1 / 2021-06-09

- Fixed: should work with typed Schema [#20](https://github.com/DouglasGabr/mongoose-lean-defaults/issues/20)

# 2.0.0 / 2021-05-12

- Fixed: should attach subdocument defaults when using projection [#18](https://github.com/DouglasGabr/mongoose-lean-defaults/issues/18) [#16](https://github.com/DouglasGabr/mongoose-lean-defaults/issues/16)
- Chore: migrate codebase to typescript
- BREAKING CHANGE: if using `require('mongoose-lean-defaults')`, you should update it to `require('mongoose-lean-defaults').default` (should not be a problem if using `import`)

# 1.0.1 / 2020-12-18

- Chore: add .npmignore to not bundle unnecessary files

# 1.0.0 / 2020-12-18

- Refactor: use Array#forEach() instead of Array#map() to improve memory usage [#14](https://github.com/DouglasGabr/mongoose-lean-defaults/pull/14) [Hafez](https://github.com/AbdelrahmanHafez)
- Fixed: handle `$slice` and `$elemMatch` projections [#12](https://github.com/DouglasGabr/mongoose-lean-defaults/pull/12) [Valeri Karpov](https://github.com/vkarpov15)
- Chore: bump version to 1.0.0, since there's no reason to keep it at 0.x, so future changes can be better represented by semver

# 0.4.1 / 2020-03-19

- Fixed: return defaults of fields which are nested inside projected object [#8](https://github.com/DouglasGabr/mongoose-lean-defaults/pull/8) [Vladimir Enchev](https://github.com/corsa1r)

# 0.4.0 / 2020-02-21

- Added: respect projection when attaching defaults

# 0.3.2 / 2020-01-02

- Fixed: old null values were breaking nested defaults

# 0.3.1 / 2019-09-28

- Added: support null value in SchemaType.default()

# 0.3.0 / 2019-09-28

- Added: support SchemaType.default() (Fixes: [#3](https://github.com/DouglasGabr/mongoose-lean-defaults/issues/3))
- Added: support nested objects without default values:
  ```javascript
  new Schema({
    obj: {
      prop: String,
    },
  });
  ```

# 0.2.0 / 2019-07-25

- Added: support default functions [#1](https://github.com/DouglasGabr/mongoose-lean-defaults/pull/1) [Valeri Karpov](https://github.com/vkarpov15)

# 0.1.1 / 2019-07-19

- Fixed: set default values in nested objects/schemas
