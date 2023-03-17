## 1: Setup react

-   Before setup react, you need to have `nodejs`
-   create react app with `vite`: (create react with vite)[https://vitejs.dev/guide/]

```bash
npm create vite@latest
```

or

```bash
npm create vite
```

-   put the `Project name` -> select framework: `react` -> select a variant: `js`
-   Then `cd react` -> `npm i` -> `npm run dev`
-   you may be config port when run `npm run dev` by config port in package.json

```json
"scripts": {
    "dev": "vite --port 3000",
  },
```

-   You can be delete **App.css**, clear all code css in **index.css**, delete `react.svg` in `src/assets`

