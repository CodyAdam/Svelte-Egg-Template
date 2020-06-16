# 🥚 Svelte Egg Template 🥚

This is a boilerplate for [Svelte](https://svelte.dev/) using [ElectronJS](https://electronjs.org/), with [Storybook](https://storybook.js.org/), [Typescript](https://www.typescriptlang.org/) and [SCSS](https://sass-lang.com/) support.

## How to create a new project using this boilerplate

```bash
npx degit "codyadam/svelte-egg-template" svelte-electron
cd svelte-electron
npm install
```

## Avaliable NPM Scripts

##### To run Electron app with live reload

```bash
npm run start:dev
```

##### To run inside the browser with live reload

```bash
npm run start:browser
```

##### To build static application

```bash
npm run build
```

The static app will be in `./public`

##### To package application

```bash
npm run package
```

Packaged app will be in `./dist/` folder.

##### To run Storybook

```bash
npm run storybook
```

Opens browser with Storybook.
Storybook root folder is `./src/stories/`

## How to use SCSS

```javascript
//inside your .svelte file
<style lang="scss"> 
  // your scss code here 
</style>
```

## How to use TypeScript

```javascript
//inside your .svelte file
<script lang="typescript"> 
  // your typescript code here 
</script>
```
