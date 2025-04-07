# vue-js-first

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


# My Vue.js Learning Notes

---

## 🧠 What is Vue.js?
- Vue.js is a JavaScript framework for building web applications.
- It is a **progressive framework**, meaning you can scale it from simple to complex.
- Vue is commonly used to build **Single Page Applications (SPA)**.

---

## 🚀 Vue Without Installation
You can use Vue.js without installing Node.js or npm:

### Steps:
1. Create an `index.html` file.
2. Create an `app.js` file.
3. Add Vue.js CDN link in `index.html`.
4. Write your Vue code in `app.js`.

### Example:
```html
<!-- index.html -->
<!DOCTYPE html>
<html>
<head>
    <title>Vue without NPM</title>
</head>
<body>
    <div id="app">
        <h1>{{ message }}</h1>
    </div>

    <script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
    <script src="app.js"></script>
</body>
</html>


## Interpolation
- {{ }} is used to insert expressions.
- You can do math: `{{ 20 + 20 }}`
- You can access variables like: `{{ name }}`

## Data vs Methods
- `data()` returns reactive variables.
- `methods` contains functions (logic).