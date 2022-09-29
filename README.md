# TailwindCSS Starter Pack With Vite

## **How To start**

### **Clone From:**

```
git clone https://github.com/ibnshayed/Tailwindcss-Starter-Pack-With-Vite.git
```

### **TailwindCss Build For Development:**

```
npm i
npm run dev

or

yarn
yarn dev
```

### **Start: On VS Code any live server**

## **How to Create this from scratch**

```
npm init -y 
npm install -D tailwindcss@latest postcss-cli@latest autoprefixer@latest vite@latest postcss-import@latest daisyui@latest

or

yarn init -y
yarn add -D tailwindcss@latest postcss-cli@latest autoprefixer@latest vite@latest postcss-import@latest daisyui@latest
```

### Tailwind Full Config

```
npx tailwind init --full ( change name to tailwind-default.config.css )
```

### Tailwind & Postcss Config

```
npx tailwind init -p
```

# tailwind.config.js

```javascript
module.exports = {
  mode: "jit",
  purge: ["./**/*.html", "./src/**/*.{js,jsx,ts,tsx,vue}"],
  plugins: [require("daisyui")],
}
```

# postcss.config.js

```javascript
module.exports = {
  plugins: {
		"postcss-import": {},
		'tailwindcss/nesting': {},
    tailwindcss: {},
    autoprefixer: {},
  },
};

```

# css/tailwind.css
```javascript
@import "tailwindcss/base";
@import "tailwindcss/components";
@import "tailwindcss/utilities";
```


# package.json

```javascript
 "scripts": {
    "dev": "vite", // start dev server
    "build": "vite build", // build for production
    "serve": "vite preview" // locally preview production build
  }
```

# vite.config.js

```javascript
import { defineConfig } from 'vite'

export default defineConfig({
  base: '/Tailwindcss-Starter-Pack-With-Vite/', // '/<REPO_NAME>/'
	server: {
		port: 4000
	}
})
```

# Deploy to GitHub Pages

```javascript

$npm run build

$git add dist -f // remove dist folder from .gitignore file

$git commit -m 'dist folder added'

$git subtree push --prefix dist origin gh-pages // adding a branch gh-pages and deploy

```
