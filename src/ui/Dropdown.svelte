<script>
    import CodeDisplay from './CodeDisplay/CodeDisplay.svelte';
    import {scss} from "svelte-preprocess";
    let displayed = false;
    const display = () => {
        displayed = !displayed;
    }
</script>

<svelte:head>
    <link rel="stylesheet" href="https://unpkg.com/mono-icons@1.0.5/iconfont/icons.css" >
</svelte:head>

    <div class="">
        <h2>Dropdown</h2>
        <div class="main_section">
        <div class="Drop">
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
                <li><a class="dropdown-item" href="#">Action</a></li>
                <li><a class="dropdown-item" href="#">Another action</a></li>
                <li><a class="dropdown-item" href="#">Something else</a></li>
            </ul>

        </div>
        </div>
            <div class="">

    <CodeDisplay tabs={[
        {label: 'App.svelte',
        value: '<Dropdown />'},
        {
          label:'Dropdown.svelte',
          value: `
          <script>
    import CodeDisplay from './CodeDisplay/CodeDisplay.svelte';
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
                <li><a class="dropdown-item" href="#">Action</a></li>
                <li><a class="dropdown-item" href="#">Another action</a></li>
                <li><a class="dropdown-item" href="#">Something else</a></li>
            </ul>
        </div>
    </div>

<style lang="scss">
    .dropdown {
        position: absolute;
        background-color: #175150;
        border-radius: 8px;
      .btn {
        display: flex;
        align-items: center;
        background-color: #175150;
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
            border-color: #175150;
          }
        }
    }
    #dropdown-menu{
      list-style-type: none;
      padding-left: 0;
      margin: 5px;
      .dropdown-item {
      color: white;
      }
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
</div>
</div>
    </div>

<style lang="scss">
  .drop {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }
  .main_section{
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 50px;
    width: 100%;
  }
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
