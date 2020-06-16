<script>
  import { tweened } from "svelte/motion";
  import { writable } from "svelte/store";

  import { quartOut } from "svelte/easing";
  import { bounceOut } from "svelte/easing";

  const rotation = tweened(0, { duration: 1000, easing: quartOut });
  const yPos = tweened(0, { duration: 500, easing: bounceOut });
  const click = writable(0);

  function handleClick() {
    $click++;
    if ($click >= 6) {
      $rotation += 360;
      $rotation = Math.round($rotation / 360) * 360;
    } else {
      $yPos = -100;
      setTimeout(() => {
        $yPos = 0;
      }, 100);
    }
  }
</script>

<style>
  main {
    position: absolute;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: #eceaea;
  }
  div {
    user-select: none;
  }
  .egg {
    font-size: 100px;
    cursor: pointer;
  }
  a {
    margin: 20px;
    text-decoration: none;
    color: rgb(175, 175, 175);
  }
  img {
    height: 25px;
    margin: 3px;
  }
</style>

<main>
  <div
    class="egg"
    style="transform: rotate({$rotation}deg) translateY({$yPos}px)"
    on:click={handleClick}>
    {#if $click <= 3}
      🥚
    {:else if $click <= 4}🐣{:else if $click <= 5}🐥{:else}🐤{/if}
  </div>
  <a href="https://github.com/CodyAdam/Svelte-Egg-Template">
    github.com/
    <strong>CodyAdam</strong>
    /Svelte-Egg-Template
  </a>
  <div class="icons">
    <img src="https://svelte.dev/favicon.png" alt="" />
    <img src="https://www.electronjs.org/images/favicon.ico" alt="" />
    <img
      src="https://storybook.js.org/images/logos/icon-storybook.png"
      alt="" />
    <img
      src="https://www.typescriptlang.org/assets/images/icons/favicon.ico"
      alt="" />
    <img src="https://sass-lang.com/favicon.ico" alt="" />
  </div>
</main>
