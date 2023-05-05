# First NPM Package (first-react-ts-npm-package-test)

[![NPM version][npm-image]][npm-url]
![npm-typescript]

This repo is the example of the article ["How to create and publish React Typescript npm package with demo and automated build"](https://medium.com/@igaponov/how-to-create-and-publish-react-typescript-npm-package-with-demo-and-automated-build-80c40ec28aca).

You can clone it and step by step create your own NPM package and publish it.

It is simple React counter.

[**Live Demo**](https://zahramirzaei.github.io/simple-npm-package/)

## Installation:

```bash
npm install react-ts-test --save-dev
```

or

```bash
yarn add -D react-ts-test
```

## Usage :

Add `MyCounter` to your component:

```js
import React from 'react'
import ReactDOM from 'react-dom/client'
import { MyCounter } from 'react-ts-test'

const root = ReactDOM.createRoot(document.getElementById('root') as HTMLElement)
root.render(
    <React.StrictMode>
        <div>
            <h2>Default counter</h2>
            <MyCounter />
        </div>
        <hr />
        <div>
            <h2>Counter with predefined value</h2>
            <MyCounter value={5} />
        </div>
    </React.StrictMode>,
)

```

[npm-url]: https://www.npmjs.com/package/react-ts-test
[npm-image]: https://img.shields.io/npm/v/react-ts-test
[github-license]: https://img.shields.io/github/license/gapon2401/react-ts-test
[github-license-url]: https://github.com/gapon2401/react-ts-test/blob/master/LICENSE
[github-build]: https://github.com/gapon2401/react-ts-test/actions/workflows/publish.yml/badge.svg
[github-build-url]: https://github.com/gapon2401/react-ts-test/actions/workflows/publish.yml
[npm-typescript]: https://img.shields.io/npm/types/react-ts-test

<hr/>

Possible error when you want to login to npm with below command in **WSL**:

`npm login`

[solution:](https://github.com/microsoft/WSL/issues/3882) (type this command into terminal and then reload vscode)

`export PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`

If you start project with above **article link** and after running `npm publish --dry-run` see error `Module ts-jest in the transform option was not found.`, you need more packages installation:

> Some of these packages should have specific versions. Just pay attention to the error description.

- [Jest](https://jestjs.io/docs/getting-started)
- [@types/jest](https://www.npmjs.com/package/@types/jest)
- [jest-environment-jsdom](https://www.npmjs.com/package/jest-environment-jsdom)
- [ts-jest](https://kulshekhar.github.io/ts-jest/docs/getting-started/installation)
- [React Testing Library](https://testing-library.com/docs/react-testing-library/intro/)
- [jest-canvas-mock](https://www.npmjs.com/package/jest-canvas-mock)
