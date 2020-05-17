## Welcome to my second package for VueJS: DaoToggle

This is the firs package I made for using with VueJS. In short, I was using this as global component in my VueJS applications. Now, I wanted to share this if anyone likes this. This is absolutely free(like other NPM packages) and easy to use. Just read more below.

### Info

| Keyword       | Description     |
| ------------- | :-------------- |
| Package name  | @dao-vue/toggle |
| Package size  | 3.2 kB          |
| Unpacked size | 10.1 kB         |
| Total files   | 3 files         |
| Live version  | 0.0.3           |

### Installation

##### To add this package to your

```bash
yarn add @dao-vue/toggle --save   # using yarn
npm i --save @dao-vue/toggle      # using npm
```

##### Including in project

```js
import DaoToggle from "@dao-vue/toggle";
import Vue from "vue";

Vue.use(DaoToggle);
```

##### Usage

###### HTML:

```html
<dao-toggle v-model="checkbox">My Toggle</dao-toggle>
```

###### JS

```js
data() {
  checkbox: false // or true
}
```

##### Notes:

Above `--save` while installation is to make sure if the toggle is installed and saved to **node_modules** folder.
And don't forget to include the package as is above in the `index.js` or `main.js` file of your project.

##### Coming soon/in the next versions

- Upgrade to new style of component sharing
- New designed toggle
- Fix: square mode
- Add: rounded, flat, square, line shadow modes
- New: color, text-color, icon-bg, icon-color attributes
- Sizes: xs, sm, md, lg, xl
- Right &/ left side text mode
- Outlined mode
- Flat mode
- Long mode
- Style and size and class attributes
- Animations(if want to use)

### Have fun with DaoToggle 😄.
