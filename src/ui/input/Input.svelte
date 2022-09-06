<script>
  import CodeDisplay from '../CodeDisplay/CodeDisplay.svelte';
  export let label;
  export let inputType;
  export let inputName;

  let value = "";

  const handleChange = (e) => {
    value = e.target.value;
    value = value;
  }
</script>


<div class="">
  <h2>Input et Label</h2>
  <div class="main_section">
    <div class="input">
      <label for={inputName}>{label}</label>
      <input type="text" name={inputName} id={inputName} bind:value={value} on:Input={handleChange}/>
      <p> Enchanté {value}</p>
    </div>
    <div class="">
      <CodeDisplay tabs={[
        {label: 'App.svelte',
        value: `<Input label="Nom" inputName="Nom"/>`
        },{
          label:'Input.svelte',
          value: `
          <script>
            export let label;
            export let inputType;
            export let inputName;

            let value = "";

            const handleChange = (e) => {
              value = e.target.value;
              value = value;
            }
          </script>
          <div class="">
            <h2>Input et Label</h2>
            <div class="input">
              <label for={inputName}>{label}</label>
              <input type="text" name={inputName} id={inputName} bind:value={value} on:Input={handleChange}/>
              <p> Enchanté {value}</p>
            </div>
          </div>

          <style>
            .input{
              display: flex;
              flex-direction: column;
              align-items: flex-start;
            }
          </style>

          `
        }]} />
    </div>
  </div>



</div>

<style>
  .main_section{
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 50px;
    width: 100%;
  }
  .input{
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }
</style>
