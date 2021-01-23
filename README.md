# Installation

```
yarn install
yarn start
```

# Start from scratch

```
yarn create react-app my-app --template typescript && cd my-app
yarn add styled-components @types/styled-components react-router-dom @types/react-router-dom react-helmet @types/react-helmet
yarn add -D babel-plugin-styled-components
```

Add `resolutions` property to package.json:

```jsx
{
  "resolutions": { 
    "styled-components": "^5"
  }
}
```

Run `yarn install`.

Create `.babelrc` file:

```jsx
//.babelrc
{
  "plugins": [ 
    ["babel-plugin-styled-components", { "ssr": true }] 
  ]
}
```

# Fork

You cannot always make a branch or pull an existing branch and push back to it,
because you are not registered as a collaborator for that specific project.

Forking is nothing more than a clone on the GitHub server side:

- without the possibility to directly push back
- with fork queue feature added to manage the merge request

You keep a fork in sync with the original project by:

- adding the original project as a remote
- fetching regularly from that original project
- rebase your current development on top of the branch of interest you got
  updated from that fetch.

[source](https://stackoverflow.com/questions/3611256/forking-vs-branching-in-github)

## Don't fork into the same account

Duplicating the repository If the new repository absolutely must be owned by the
same account, you can duplicate the repository. This creates a new repository
that starts out identical to the original repository but is not a fork. For more
information, see
[Duplicating a repository](https://help.github.com/articles/duplicating-a-repository/).

Because the new repository is not a fork, you won’t be able to create pull
requests between the two repositories. However, you can still push and pull
changes between the two repositories by adding the original repository as remote
for the new repository. For more information, see
[Adding a remote](https://help.github.com/articles/adding-a-remote/).

[source](https://github.community/t/alternatives-to-forking-into-the-same-account/10200)

## Duplicate repository

- `git clone --bare https://github.com/Luk-z/react-typescript-styled-router-starter-kit.git`
- `cd react-typescript-styled-router-starter-kit`
- `git push --mirror https://github.com/Luk-z/react-typescript-styled-router-starter-kit-NEW.git`
- `cd ..`
- `rm -rf react-typescript-styled-router-starter-kit`

[source](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/duplicating-a-repository)

# Getting Started with Create React App

This project was bootstrapped with
[Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `yarn test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests)
for more information.

### `yarn build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best
performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about
[deployment](https://facebook.github.io/create-react-app/docs/deployment) for
more information.

### `yarn eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can
`eject` at any time. This command will remove the single build dependency from
your project.

Instead, it will copy all the configuration files and the transitive
dependencies (webpack, Babel, ESLint, etc) right into your project so you have
full control over them. All of the commands except `eject` will still work, but
they will point to the copied scripts so you can tweak them. At this point
you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for
small and middle deployments, and you shouldn’t feel obligated to use this
feature. However we understand that this tool wouldn’t be useful if you couldn’t
customize it when you are ready for it.

## Learn More

You can learn more in the
[Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).
