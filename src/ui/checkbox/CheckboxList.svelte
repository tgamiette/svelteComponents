<script>
    import Checkbox from './Checkbox.svelte';
    import CodeDisplay from '../CodeDisplay/CodeDisplay.svelte';
  
</script>
  
  <h2>Checkbox</h2>
  <section class="checkbox">
    <Checkbox
        content = "Indiquez votre contenu !"
    />   
      <CodeDisplay tabs={[
        {label: 'App.svelte',
        value: `
          <script>
            import Checkbox from './Checkbox.svelte';
          </script>
          <Checkbox
          content = "Indiquez votre contenu !"
          />`
        },{
          label:'Checkbox.svelte',
          value: `
          <script>
            let isActive = false;
            export let content = "";

            const check = () => {
                isActive = !isActive;
            };
          </script>
  
          <form>
            <input type="checkbox" id="confirm" name="confirm" on:click={ check }>
            <label for="confirm">{ content }</label>
          </form>
  
          `
        }]} />
  
  
  </section>
  
  <style>
  
    .checkbox{
      display: grid;
      grid-template-columns: 1fr 1fr;
      grid-gap: 50px;
      width: 100%;
    }
  
  </style>
  