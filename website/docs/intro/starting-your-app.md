---
id: final-parts
title: Final Parts
sidebar_label: Final Parts
---

You'll be pleased to know we are almost ready to start writing some real code!

## Fixing ESLint or Prettier errors

A lot of ESLint and all Prettier errors can be fixed automatically so we'll quickly go over this. Open ```serviceWorker.ts``` to look over the new violations.

If the rule has a 'fixer' you will have a tooltip option inside Visual Studio Code to automatically fix the issue. Howver earlier on we set up a fix all code action on save so you can test that out now by simply hitting save! If it cannot be fixed automatically you can always jump straight to the documentation for the error:

![Fix Prettier Error](/img/intro-fix-prettier.png)

## TypeScript Upgrade

Before we start coding we can bump TypeScript to the latest version in case our create react app is behind

```base npm2yarn
npm install typescript
```

## Clean Up Operation!

As a learning exercise we should start our applications code base from scratch and add parts in as we need. To do this lets delete a few of the files in the ```src``` folder!

```bash
cd my-app
cd src

# If you're using a Mac:
rm -f App.css App.tsx App.test.tsx logo.svg

# Or, if you're on Windows:
del App.css App.tsx App.test.tsx logo.svg

# Then, switch back to the project folder
cd ..
```
