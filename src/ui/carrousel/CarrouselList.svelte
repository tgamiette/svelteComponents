<script>
  import Carrousel from './Carrousel.svelte';
  import CodeDisplay from '../CodeDisplay/CodeDisplay.svelte';
</script>

<section class="carrouselCard">
  <div class="">
    <Carrousel 
    imgs = {
      ["https://cdn.pixabay.com/photo/2015/07/10/16/05/purple-flowers-839594_1280.jpg",
      "https://cdn.pixabay.com/photo/2018/06/16/20/44/lavenders-3479492_1280.jpg",
      "https://cdn.pixabay.com/photo/2012/03/04/00/35/garden-21968_1280.jpg"]
      }
    />
  </div>

  <CodeDisplay tabs={[
      {label: 'App.svelte',
      value: `
        <script>
          import Carrousel from '../carrousel/Carrousel.svelte';
        </script>
        <Carrousel/>
`
      },{
        label:'Carrousel.svelte',
        value: `
        <script>    
    export let imgs = [];

    let currentImg = 0;
  
    const prevImg = () => {
      currentImg -= 1;
  
      if (currentImg < 0) {
        currentImg = imgs.length - 1;
      }
    };
  
    const nextImg = () => {
      currentImg += 1;
  
      if (currentImg > imgs.length - 1) {
        currentImg = 0;
      }
    };
  
  </script>
  
  <figure>
    <img src={ imgs[currentImg] } alt="carrousel" id="img" >
  </figure>
  
  <nav>
    <button on:click={ prevImg }>
      preview
    </button>
    <button on:click={ nextImg }>
      next
    </button>
  </nav>
  
  <style>
    #img {
      width: 500px;
    }
  </style>
        `
      }]}/>


</section>

<style>
    .carrouselCard {
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-gap: 50px;
        width: 100%;
    }

</style>
