**Tailwind Installation:**

```shell
yarn add @nuxtjs/tailwindcss -D
```

New file **tailwind.css** in **assets/styles**

```css
@import "tailwindcss/base";
@import "tailwindcss/components";
@import "tailwindcss/utilities";
```

New file **tailwind.config.ts** in **assets/styles**

```javascript
module.exports = {
  content: ["./pages/**/*.{vue}", "./components/**/*.{vue}"],
  theme: {},
};
```

In nuxt.config.ts, add the following properties:

```javascript
modules: ["@nuxtjs/tailwindcss"],
tailwindcss: {
  cssPath: "~/assets/styles/tailwind.css",
  configPath: "./assets/styles/tailwind.config",
  exposeConfig: false,
  exposeLevel: 2,
  config: {},
  injectPosition: "first",
  viewer: true,
},
```
