# ⚛️ React + ⚡ TypeScript + 🚀 Vite

Шаблон для быстрого старта с React + Vite + ESLint + HMR.

## 🔧 Плагины

* 🧪 [`@vitejs/plugin-react`](https://github.com/vitejs/vite-plugin-react) — через **Babel**
* ⚡ [`@vitejs/plugin-react-swc`](https://github.com/vitejs/vite-plugin-react) — через **SWC**

## ✅ ESLint с проверкой типов

```js
export default tseslint.config([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      ...tseslint.configs.recommendedTypeChecked,
      // или:
      // ...tseslint.configs.strictTypeChecked,
      // + стилистика:
      // ...tseslint.configs.stylisticTypeChecked,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
    },
  },
])
```

## ⚛️ Доп. правила для React

Установи:

* [`eslint-plugin-react-x`](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x)
* [`eslint-plugin-react-dom`](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom)

```js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default tseslint.config([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      reactX.configs['recommended-typescript'],
      reactDom.configs.recommended,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
    },
  },
])
```