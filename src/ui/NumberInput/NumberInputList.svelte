<script>
  import NumberInput from '../NumberInput/NumberInput.svelte';
  import CodeDisplay from '../CodeDisplay/CodeDisplay.svelte';
</script>

<section class="numberCard">
  <NumberInput/>
  <CodeDisplay tabs={[
      {label: 'App.svelte',
      value: `
        <script>
            import NumberInput from './NumberInput/NumberInput.svelte';
        </script>
        <NumberInput/>
`
      },{
        label:'NumberInput.svelte',
        value: `
<script>
  let index = 0;
  const Plus = () => {
    index += 1;
  };
  const Moins = () => {
    if (index <= 0) {
      return;
    }
    index -= 1;
  };
</script>
<div class="">
    <button on:click= { Moins } >-</button>
<label>
  <input class="input" bind:value={ index }>
</label>
  <button on:click={ Plus } >+</button>
</div>
        `
      }]}/>


</section>

<style>
    .numberCard {
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-gap: 50px;
        width: 100%;
    }

</style>
