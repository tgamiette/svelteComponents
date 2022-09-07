<script>
  import svelteLogo from './assets/svelte.svg';
  import Counter from './lib/Counter.svelte';
  import CheckboxList from './ui/checkbox/CheckboxList.svelte';
  import CalendarList from './ui/calendar/CalendarList.svelte';
  import ModalAlert from './ui/ModalAlert.svelte';
  import ProductList from './ui/productList/ProductList.svelte';
  import Input from './ui/input/Input.svelte';
  import Carrousel from './ui/Carrousel.svelte';
  import Numberinput from './ui/Numberinput.svelte';
  import AnimateButtonList from "./ui/animateButton/AnimateButtonList.svelte";
  import Dropdown from "./ui/Dropdown.svelte";
  import Navbar from './ui/navbar/NavbarList.svelte';

</script>

<main>

  <div class="checkboxList">
    <CheckboxList />
  </div>

  <div class="calendar">
    <CalendarList/>
  </div>

  <div class="productList">
    <ProductList />
  </div>

  <div class="Input">
    <Input label="Nom" inputName="Nom"/>
  </div>

  <div class="productList">
    <AnimateButtonList />
  </div>

  <div class="Dropdown">
    <Dropdown />
  </div>

  <div class="Dropdown">
    <h2>Modal Alert</h2>
    <ModalAlert />
  </div>

  <div class="Dropdown">
    <h2>Carrousel</h2>
    <Carrousel
    imgs = {
    ["https://cdn.pixabay.com/photo/2015/07/10/16/05/purple-flowers-839594_1280.jpg",
    "https://cdn.pixabay.com/photo/2018/06/16/20/44/lavenders-3479492_1280.jpg",
    "https://cdn.pixabay.com/photo/2012/03/04/00/35/garden-21968_1280.jpg"]
    }
  />
  </div>

  <div class="Dropdown">
    <h2>Counter</h2>
    <Numberinput />
  </div>

  <div class="Navbar">
    <h2>Navbar</h2>
    <Navbar />
  </div>

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
