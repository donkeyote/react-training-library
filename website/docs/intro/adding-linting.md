---
id: adding-linting
title: Adding Linting
---

Explain eslint and its uses???

Create React App comes with a default eslint config _react-app_. This gives us an excellent starting point, including the _react-hooks/rules-of-hooks_ package (the [Rules of Hooks](https://reactjs.org/docs/hooks-rules.html) will become more apparent as we progress), which will be important when writing modern react applications. 

However there are times when you will need to override or extend this default ruleset. We will cover how this is done now.

## Extending ESLint Config

To extend the ESLint config we first need to create a new file ```.env``` in the root of our project. [dotenv](https://github.com/motdotla/dotenv/blob/master/README.md) is included as a dependency in Create React App and these files can be used to drive your applications environment variables, i.e. dev, test and live (more on that later!). For now open the new file and add the following:

```
EXTEND_ESLINT=true
```

Now create another new file ```.eslintrc.json``` in the root of our project. Open that file up and add the following:

```code
{
  "extends": [
    "react-app"
  ]
}
```

By extending the ```react-app``` config we are taking the default config, mentioned above, as our starting point.

As we are using TypeScript in this application we can add the TypeScript ESLint recommended settings which will give us a stronger set of base rules:

```diff
{
  "extends": [
-   "react-app"
+   "react-app",
+   "plugin:@typescript-eslint/recommended"
  ]
},
```

The ```typescript-eslint``` package is included already from Create React App so there is no need to add any new dependencies. The recommended rules which this will have turned on can be found [here](https://github.com/typescript-eslint/typescript-eslint/blob/master/packages/eslint-plugin/src/configs/recommended.json).

We can also change any particular rule by adding another ```rules``` property to our config:

```diff
"eslintConfig": {
  "extends": [
    "react-app",
    "plugin:@typescript-eslint/recommended"
- ]
+ ],
+ "rules": {
+   "@typescript-eslint/explicit-function-return-type": "off"
+ }
},
```

Lint errors will continue to be shown in your terminal or browser when the ```start``` or ```build``` scripts are run.
