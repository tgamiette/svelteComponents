<script>
  import CheckboxList from './ui/checkbox/CheckboxList.svelte';
  import CalendarList from './ui/calendar/CalendarList.svelte';
  import ModalAlertList from './ui/modalAlert/ModalAlertList.svelte';
  import ProductList from './ui/productList/ProductList.svelte';
  import Input from './ui/input/Input.svelte';
  import CarrouselList from './ui/carrousel/CarrouselList.svelte';
  import AnimateButtonList from "./ui/animateButton/AnimateButtonList.svelte";
  import Dropdown from "./ui/Dropdown.svelte";
  import NavbarList from './ui/navbar/NavbarList.svelte';
  import NumberInputList from "./ui/NumberInput/NumberInputList.svelte";

</script>

<main>
  <div class="card">
    <h1>Composants Svelte</h1>
    <div class="checkboxList">
      <CheckboxList />
    </div>
  </div>

  <div class="card">
    <div class="calendar">
      <CalendarList/>
    </div>
  </div>

  <div class="card">
    <div class="productList">
      <ProductList />
    </div>
  </div>

  <div class="card">
    <div class="Input">
      <Input label="Nom" inputName="Nom"/>
    </div>
  </div>

  <div class="card">
    <div class="productList">
      <AnimateButtonList />
    </div>
  </div>

  <div class="card">
    <div class="Dropdown">
      <Dropdown />
    </div>
  </div>

  <div class="card">
    <div class="ModalAlert">
      <ModalAlertList />
    </div>
  </div>

  <div class="card">
    <div class="Carrousel">
      <h2>Carrousel</h2>
      <CarrouselList />
    </div>
  </div>
  
  <div class="card">
    <div class="Counter">
      <h2>Counter</h2>
      <NumberInputList />
    </div>
  </div>

  <div class="card">
    <div class="Navbar">
      <NavbarList />
    </div>
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
