---
title: no-octal-escape
rule_type: suggestion
---


As of the ECMAScript 5 specification, octal escape sequences in string literals are deprecated and should not be used. Unicode escape sequences should be used instead.

```js
const foo = "Copyright \251";
```

## Rule Details

This rule disallows octal escape sequences in string literals.

If ESLint parses code in strict mode, the parser (instead of this rule) reports the error.

Examples of **incorrect** code for this rule:

::: incorrect  { "sourceType": "script" }

```js
/*eslint no-octal-escape: "error"*/

const foo = "Copyright \251";
```

:::

Examples of **correct** code for this rule:

::: correct  { "sourceType": "script" }

```js
/*eslint no-octal-escape: "error"*/

const foo = "Copyright \u00A9";   // unicode

const buz = "Copyright \xA9";     // hexadecimal
```

:::
