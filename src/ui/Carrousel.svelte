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