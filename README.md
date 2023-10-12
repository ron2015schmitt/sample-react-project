# Sample React Project With Tools 2023

Tools / packages

- [React 18](https://legacy.reactjs.org/blog/2022/03/29/react-v18.html)
- nvm
- nodejs 18.18
- npm 10.2
- pnpm 8.9
- vite 4.4
- elint 8.45
- TypeScript 5.0
- SWC 3.3

## install

### Package manager setup.

```bash
nvm install 18.18
nvm use 18.18
npm i -g npm@10.2
npm i -g pnpm@8.9
```
 
### Clone repo

```bash
git clone https://github.com/ron2015schmitt/sample-react-project.git
cd sample-angular-project
```

### Install packages

```bash
pnpm install
```
### Run

```bash
pnpm run dev
```
point browser to http://localhost:5173/

![image](https://github.com/ron2015schmitt/sample-react-project/assets/11559541/3a85c3a1-793f-4000-8f0d-ca6b599cca1c)


## How this repo was created
### Set up package managers: nvm, npm, pnpm

```bash
nvm install 18.18
nvm use 18.18
npm i -g npm@10.2
npm i -g pnpm@8.9
```

### Create React Project using pnpm and vite

```bash
pnpm create vite sample-react-project
```

You be asked to choose a **framework** -> React

![image](https://github.com/ron2015schmitt/sample-react-project/assets/11559541/af8e5699-ae89-43b7-b0f0-cc7fa880a736)


and a **variant** -> TypeScript + SWC

![image](https://github.com/ron2015schmitt/sample-react-project/assets/11559541/7e36e357-8519-40cf-aa22-4189aa0c6976)

### Add engines section to the `package.json`

Add the tool versions to `package.json`, which will get enforced during build.

```json
  "engines": {
    "node": "18.18",
    "npm": "10.2",
    "pnpm": "8.9"
  },
```

### verify the build
```bash
cd sample-react-project
pnpm install
pnpm run dev
```



## Notes provided by the pnpm Vite installer

### React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

### Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type aware lint rules:

- Configure the top-level `parserOptions` property like this:

```js
   parserOptions: {
    ecmaVersion: 'latest',
    sourceType: 'module',
    project: ['./tsconfig.json', './tsconfig.node.json'],
    tsconfigRootDir: __dirname,
   },
```

- Replace `plugin:@typescript-eslint/recommended` to `plugin:@typescript-eslint/recommended-type-checked` or `plugin:@typescript-eslint/strict-type-checked`
- Optionally add `plugin:@typescript-eslint/stylistic-type-checked`
- Install [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react) and add `plugin:react/recommended` & `plugin:react/jsx-runtime` to the `extends` list
