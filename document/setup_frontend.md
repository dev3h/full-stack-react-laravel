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

## 2: Setup Construct folder

```
src
├── views
├── components
|-- contexts
```

---

## 3: React router dom

-   remember you stand in react folder to install

```bash
npm i react-router-dom
```

### 3.1: Setup router

-   [tutorial](https://reactrouter.com/en/main/start/tutorial)
-   create file `src/router.jsx` with use **createBrowserRouter**
-   Then we use it in `main.jsx` with _RouteProvider_ and pass `router` to it
-   Note:
    -   route `*` is a default route
    -   `<Outlet />` should be used in parent route elements to render their child route element

---

## 4: Setup Context

-   create ContextProvider in `src/contexts/ContextProvider.jsx`
-   then you need to wrap `ContextProvider` in `main.jsx` with `RouteProvider`

---

## 5: Install Axios to call Api

-   [axios doc](https://axios-http.com/docs/intro)

```bash
npm install axios
```

### 5.1: Setup axios

-   create file `src/axios-client.js` with config axios

#### env

-   use env variable in vite: [vite env](https://vitejs.dev/guide/env-and-mode.html)
-   create file `react/.env.example` to example config url api.
-   create file `react/.env` to config url api. This is a main setup env. When you want update env, you need update in `.env` not `.env.example`, `.env.example` is a example for other developer to know what env you need to config in `.env`. `env` is ignored by git
#### interceptor axios
- intercept requests or responses before they are handled by then or catch