### First NPM Package

> for more description visit [THIS LINK](https://betterprogramming.pub/how-to-create-and-publish-react-typescript-npm-package-with-demo-and-automated-build-80c40ec28aca). **[Guide link]**

#### Probably error when you want to login to npm with below command in **WSL**:

`npm login`

#### [solution:](https://github.com/microsoft/WSL/issues/3882) (type this command into terminal and reload it)

`export PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`

If you start project with above **Guide Link** and after running `npm publish --dry-run` see error `Module ts-jest in the transform option was not found.`, you need more packages installation:

> Some of these packages should have specific versions. Just pay attention to the error description.

- [Jest](https://jestjs.io/docs/getting-started)
- [@types/jest](https://www.npmjs.com/package/@types/jest)
- [jest-environment-jsdom](https://www.npmjs.com/package/jest-environment-jsdom)
- [ts-jest](https://kulshekhar.github.io/ts-jest/docs/getting-started/installation)
- [React Testing Library](https://testing-library.com/docs/react-testing-library/intro/)
- [jest-canvas-mock](https://www.npmjs.com/package/jest-canvas-mock)
