<script>
  import CodeDisplay from '../CodeDisplay/CodeDisplay.svelte';
  import AnimateButton from "./AnimateButton.svelte";

</script>

<h2>Animate Button List</h2>
<section class="productCard">
  <div class="exemple">
    <AnimateButton animation="slide-left" type="submit" label="slide-left"/>
    <AnimateButton animation="slide-right" type="submit" label="slide-right"/>
  </div>
    <CodeDisplay tabs={[
      {label: 'App.svelte',
      value: `
        <script>
          import AnimateButton from "./AnimateButton.svelte";
        </script>
          <AnimateButton animation="slide-left" type="submit" label="slide-left"/>
          <AnimateButton animation="slide-right" type="submit" label="slide-right"/>
`
      },{
        label:'AnimateButton.svelte',
        value: `
<script>
  export let colorBtn = '#234db6'
  export let fontColor = '#f8f8f8'
  export let slideColor = '#f8f8f8'
  export let type = 'button'
  export let label = 'Ceci est un bouton'
  export let animation = "slide-right"
</script>
        <style>

         .productCard{
           width: 40%;
           background: #ffffff;
           box-shadow: 0px 0px 20px 1px rgba(0, 0, 0, 0.1);
           border-radius: 1rem;
           display: flex;
           flex-direction: column;
           position: relative;
         }


         .productCard_img, .productCard_img img{
           width: 100%;
         }

         .productCard_img img{
           border-radius: 1rem 1rem 0 0;
         }

         .productCard_infos{
            padding: 20px;
         }

         .productCard_row {
           display: flex;
           flex-direction: row;
           justify-content: space-around;
           align-items: center;
         }

         .productCard_row a{
           border: 1px solid #7fa5d6;
           background: #7fa5d6;
           color: white;
           transition: 0.3s ease-in;
           padding: 10px 20px;
           border-radius: 10px;
         }

         .productCard_row a:hover{
           background: transparent;
           color: #7fa5d6;
         }

         .productCard_row span{
           font-weight: bold;
           font-size: 1.2rem;
         }

        </style>

        `
      }]} />


</section>

<style>

  .productCard{
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 50px;
    width: 100%;
  }

</style>
