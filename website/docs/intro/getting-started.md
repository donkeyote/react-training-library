---
id: getting-started
title: Getting Started
---

To begin this tutorial we will use [Create React App](https://create-react-app.dev/) to generate our application. This will allow us to focus immediately on code and not build tools. We will, however, cover adding your own coding standards to the created application.

## Prequistites

- Node: >= 8.10
- npm or Yarn

## Create React App

At this point you should familiarise yourself with the [Getting Started](https://create-react-app.dev/docs/getting-started) guide for Create React App.

But to begin with we simply need to run the command below, where *my-training-app* will be the name of the folder that will be created to house the application, and specify we wish to use TypeScript. 

```bash
npx create-react-app my-training-app --template typescript
cd my-training-app
```

## Starting the Application

If you have Yarn installed, Create React App will have used Yarn to install the dependencies, otherwise npm will be used. Throughout the tutorial we will try to provide commands for both package managers.

```bash npm2yarn
npm run start
```

If everything has gone according to plan the development server should start and your default browser opened up pointing to http://localhost:3000/. Congratulations! Use ```CTRL+C``` on Windows or ```control+c``` on Mac to stop the development server.

Now we can move on to setting up our Editor.

