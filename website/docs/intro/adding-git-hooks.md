---
id: adding-git-hooks
title: Adding Git Hooks
---

If you are using Git for your version control, this next section will show you how to add [githooks](https://git-scm.com/docs/githooks) to make sure your build is error free before you commit your changes.

We will introduce another tool, [husky](https://github.com/typicode/husky), which makes Git Hooks easy to use:

```bash npm2yarn
npm install husky
```

In this instance we will add a [pre-commit](https://git-scm.com/docs/githooks#_pre_commit) hook. Open your ```package.json``` file and add the following section:

```bash npm2yarn
"husky": {
  "hooks": {
    "pre-commit": "npm run build"
  }
}
```

