# 🥚 Svelte Egg Template 🥚

![Thumbnail](https://github.com/CodyAdam/Svelte-Egg-Template/blob/master/Thumbnail.png?raw=true)

This is a boilerplate for [Svelte](https://svelte.dev/) using [ElectronJS](https://electronjs.org/), with [Storybook](https://storybook.js.org/), [Typescript](https://www.typescriptlang.org/) and [SCSS](https://sass-lang.com/) support.

## How to create a new project using this boilerplate

```bash
npx degit "codyadam/svelte-egg-template" project-name
cd project-name
npm install --silent
```

This required [Git](https://git-scm.com/) to be installed.

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

The static app build will be in `./public` folder.

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
The root folder is `./src/stories/`.

## How to use SCSS

```html
<!-- inside your .svelte file -->
<style lang="scss">
    /* your scss code here */
</style>
```

## How to use TypeScript

```html
<!-- inside your .svelte file -->
<script lang="typescript">
    /* your typescript code here */
</script>
```
