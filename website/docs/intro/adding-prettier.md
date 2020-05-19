---
id: adding-prettier
title: Adding Prettier
---

While ESLint is used to find and fix potential problems in your code, [Prettier](https://prettier.io/) is used to format your code consistently. This will allow you to set a code style to be used across your application saving you time and arguments!

## Install Prettier

Run the following to save an exact version of prettier to avoid any changes that may be introduced in minor updates:

```bash npm2yarn
npm install --save-exact prettier 
```

## Integrating with ESLint

To integrate Prettier into ESLint we need to add another two more packages:

```bash npm2yarn
npm install eslint-config-prettier eslint-plugin-prettier
```

```eslint-config-prettier``` will disble any ESLint rules that conflict with Prettier, while ```eslint-plugin-prettier``` adds a rule we can use to format our code and apply fixes.

To enable this integration open the ```.eslintrc.json``` file and add the following:

```diff
{
  "extends": [
    "react-app",
-   "plugin:@typescript-eslint/recommended"
+   "plugin:@typescript-eslint/recommended",
+   "prettier"
  ],
+ "plugins": ["prettier"],
  "rules": {
-   "@typescript-eslint/explicit-function-return-type": "off"
+   "@typescript-eslint/explicit-function-return-type": "off",
+   "prettier/prettier": "error"
  }
}
```

Again we are just extending our base config and adding the Prettier plugin with a new rule to show an ```error``` for any violations. 

## Prettier Setup

Create another new file ```.prettierrc.json``` in the root of our project, which will be used to house our rules. Open that file up and add the following:

```code
{
  "trailingComma": "es5",
  "tabWidth": 2,
  "semi": true,
  "singleQuote": true,
  "printWidth": 80
}
```

You can look over the various options and theirt descriptions [here](https://prettier.io/docs/en/options.html) and tweak this to find a code style you are happy with. For example you may want to allow for longer line lengths than 80 characters and choose double quotes over single quotes for strings. Or maybe you even prefer tabs over spaces :grimacing:! The importance of Prettier is to ensure that your rules are always followed by each developer on your code base.

I would however always recommend keeping the ```trailingComma``` setting as this will improve the clarity of your diffs and commit history when adding or removing items in objects and arrays.



