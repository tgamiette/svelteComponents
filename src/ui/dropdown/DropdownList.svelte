<script>
    import Dropdown from "./Dropdown.svelte";
    import CodeDisplay from "../CodeDisplay/codeDisplay.svelte";
</script>
<svelte:head>
    <link rel="stylesheet" href="https://unpkg.com/mono-icons@1.0.5/iconfont/icons.css" >
</svelte:head>
<h2>Dropdown</h2>
<section class="main_section">
    <div class="example">
        <Dropdown texts={["Nav"]} />
    </div>
    <CodeDisplay tabs={[
        {label: 'App.svelte',
        value: '<Dropdown />'},
        {
          label:'Dropdown.svelte',
          value: `
          <script>
    import CodeDisplay from './CodeDisplay/CodeDisplay.svelte';
    export let texts = [];
    let displayed = false;
    const display = () => {
        displayed = !displayed;
    }
</script>

<svelte:head>
    <link rel="stylesheet" href="https://unpkg.com/mono-icons@1.0.5/iconfont/icons.css" >
</svelte:head>

    <div class="col-sm-4 ">
        <div class="dropdown">
            <button class="btn btn-secondary" type="button" on:click={display}>
                <span>Dropdown</span>
                <span class="icon is-small">
                    {#if displayed === false}
                    <i class="mi mi-caret-down"><span class="u-sr-only"></span></i>
                    {:else}
                    <i class="mi mi-caret-up"><span class="u-sr-only"></span></i>
                    {/if}
                </span>
            </button>
            <ul id="dropdown-menu" class:dropdown-menu-enable={displayed} class:dropdown-menu-disable={!displayed}>
                {#each texts as data}
                <li><a class="dropdown-item" href="#">{ data }</a></li>
                {/each}
                <li><a class="dropdown-item" href="#">Action</a></li>
                <li><a class="dropdown-item" href="#">Another action</a></li>
                <li><a class="dropdown-item" href="#">Something else</a></li>
            </ul>
        </div>
    </div>

<style lang="scss">
.dropdown {
    position: absolute;
    background-color: #ffb72a;
    border-radius: 8px;
    .btn {
      display: flex;
      align-items: center;
      .mi {
        display: flex;
        vertical-align: center;
        margin-left: 10px;
      }
      &:focus {
        outline: none;
      }
    }
    &:hover {
      button {
        border-color: transparent;
      }
    }
  }
  #dropdown-menu{
    list-style-type: none;
    padding-left: 0;
    margin: 5px;
    animation: growDown 200ms ease-in-out forwards;
    transform-origin: top center;
    &.dropdown-menu-enable {
      display: block;
    }
    &.dropdown-menu-disable {
      display: none;
    }
  }

  @keyframes growDown {
    0% {
      transform: scaleY(0)
    }
    80% {
      transform: scaleY(1.1)
    }
    100% {
      transform: scaleY(1)
    }
  }
</style>

          `
}]} />
</section>

<style lang="scss">
  .main_section{
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 50px;
    width: 100%;
  }
</style>
