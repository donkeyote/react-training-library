---
id: setting-up-your-editor
title: Setting Up Your Editor
sidebar_label: Editor Setup
---

## Visual Studio Code

Install the [ESLint plugin](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint#overview). This plugin will ensure that all linting issues are shown inside Visual Studio Code and if the lint error is fixable, you can apply the fix automatically.

Certain lint errors we will configure can be fixed automatically and we can enable VS Code to fix these on save.
Open your settings.json and add

```
"editor.codeActionsOnSave": {
    "source.fixAll": true
}
```