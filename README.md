\***_Eslint Steps_**

1. npm i -D eslint
2. npx eslint --init
<!-- Install airbnb config  https://www.npmjs.com/package/eslint-config-airbnb-->
3. npx install-peerdeps --dev eslint-config-airbnb
4. in .eslintrc.cjs extends replace eslint:recommended with "airbnb", "airbnb/hooks"
<!-- Install airbnb config typescript -->
5. npm i -D eslint-config-airbnb-typescript
6. in in .eslintrc.cjs extends add 'airbnb-typescript' (read repo or documentation)

**_Prettier Setup_**
install

1. npm install --save-dev eslint-config-prettier eslint-plugin-prettier.
   <!-- configuration file -->
2. add prettier.cjs https://prettier.io/docs/en/configuration
<!--Integrating with Linters  -->
3. add prettier to plugins in eslintrc.cjs https://github.com/prettier/eslint-plugin-prettier
4. Then you need to add plugin:prettier/recommended as the last extension in your .eslintrc.json:

# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

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
