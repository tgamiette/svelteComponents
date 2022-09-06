<script>
  import ProductList from './ui/productList/ProductList.svelte';
</script>

<main>
  <ProductList />
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
