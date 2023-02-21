# @nextcloud/typings
[![NPM package](https://img.shields.io/npm/v/@nextcloud/typings?style=for-the-badge)](https://www.npmjs.com/package/@nextcloud/typings)
[![License](https://img.shields.io/npm/l/@nextcloud/typings?color=green&style=for-the-badge)](https://github.com/nextcloud/nextcloud-typings/blob/master/LICENSE)
[![Open issues](https://img.shields.io/github/issues-raw/nextcloud/nextcloud-typings?style=for-the-badge)](https://github.com/nextcloud/nextcloud-typings/issues)

Versioned typings for the (internal) JavaScript APIs of Nextcloud used in higher level packages.

## Usage

You can use this package to verify your API usage is compatible with a range of Nextcloud versions

```ts
/// <reference types="@nextcloud/typings" />

declare var OC: Nextcloud.v22.OC | Nextcloud.v23.OC | Nextcloud.v24.OC;

OC.L10N.translate("app", "text")
```

The TypeScript compiler will translate the code above to `OC.L10N.translate("app", "text");` and throws an error if any of the Nextcloud versions in use for the [union type](https://www.typescriptlang.org/docs/handbook/advanced-types.html#union-types) do not exist on all interfaces.
