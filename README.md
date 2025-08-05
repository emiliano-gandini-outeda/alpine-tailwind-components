# Alpine Tailwind Components

A personal collection of reusable UI components built with **Alpine.js** and **Tailwind CSS**, optimized for use in **Next.js** projects. These components speed up frontend development with ready-to-use, responsive, and interactive UI elements.

---

## Usage Instructions

### Clone the repo
```bash
git clone https://github.com/your-username/alpine-tailwind-components.git
```

---

## Tailwind CSS Setup in Next.js

### Install Tailwind CSS and dependencies

```bash
npm install -D tailwindcss@^3.0.0 postcss autoprefixer
```

### Initialize Tailwind config files

```bash
npx tailwindcss init -p
```

### Configure tailwind.config.js

```js
/** 
 * tailwind.config.js
 * Tell Tailwind where to look for class names
 */
module.exports = {
  content: [
    './pages/**/*.{js,ts,jsx,tsx}',           // Next.js pages
    './components/**/*.{js,ts,jsx,tsx}',      // Your React components
    './alpine-tailwind-components/**/*.{html,js}'  // This repo's components if used directly
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

### Create or update global CSS file

```css
/* styles/globals.css */
/* Import Tailwind's base styles, components, and utilities */
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### Import global CSS in Next.js app

```js
// pages/_app.js
import '../styles/globals.css'

export default function App({ Component, pageProps }) {
  return <Component {...pageProps} />
}
```

---

## Alpine.js Setup

### Add Alpine.js CDN in your app

Include this script tag in your main HTML template or `_document.js` for Next.js:

```html
<script src="https://cdn.jsdelivr.net/npm/alpinejs@3.x.x/dist/cdn.min.js" defer></script>
```

---

## Development: Running Tailwind in Watch Mode

### Run Tailwind CLI to watch for CSS changes

```bash
# Adjust input/output paths according to your project structure
npx tailwindcss -i ./src/styles.css -o ./dist/output.css --watch
```

---

## How to Use Components

Copy the components you need from this repo into your project. The components use Tailwind CSS classes and Alpine.js directives for interactivity.

---

## License

See (License)[LICENSE]
