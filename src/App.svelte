<script>
  import svelteLogo from './assets/svelte.svg'
  import Counter from './lib/Counter.svelte'
  import AnimateButton from "./ui/AnimateButton.svelte";
</script>

<main>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite Logo" />
    </a>
    <a href="https://svelte.dev" target="_blank">
      <img src={svelteLogo} class="logo svelte" alt="Svelte Logo" />
    </a>
  </div>
  <h1>Vite + Svelte</h1>
  <AnimateButton animation="slide-left" type="submit" label="slide-left"/>
  <AnimateButton animation="slide-right" type="submit" label="slide-right"/>


  <div class="card">
    <Counter />
  </div>

  <div class="checkbox">
    <Checkbox
      content = "Indiquez votre contenu !"
    />
  </div>

  <div class="calendar">
    <Calendar/>
  </div>

  <div class="productList">
    <ProductList />
  </div>

  <div class="Input">
    <Input label="Nom" inputName="Nom"/>
  </div>

  <AnimateButton animation="slide-left" type="submit" label="slide-left"/>

  <AnimateButton animation="slide-right" type="submit" label="slide-right"/>

  <AnimateButton animation="slide-blob" type="submit" label="slide-blob"/>

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