<script>
  import svelteLogo from './assets/svelte.svg'
  import Counter from './lib/Counter.svelte'
  import AnimateButton from "./ui/AnimateButton.svelte";
</script>


<main>
  <AnimateButton animation="slide-left" type="submit" label="slide-left"/>

  <AnimateButton animation="slide-right" type="submit" label="slide-right"/>

  <AnimateButton animation="slide-blob" type="submit" label="slide-blob"/>
</main>

<style lang="scss">
  $color: purple;

  .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
  }

  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }

  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }

  .read-the-docs {
    color: #888;
  }
</style>
