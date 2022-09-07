<script>
  import ProductCard from './ProductCard.svelte';
  import CodeDisplay from '../CodeDisplay/CodeDisplay.svelte';

</script>

<h2>Product List</h2>
<section class="productCard">
    <ProductCard
      title="Casque audio bluetooth"
      description="Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident."
      link="#"
      image="/public/produtc_img.jpg"
      price="78"
      color="#ffc239"
    />

    <CodeDisplay tabs={[
      {label: 'App.svelte',
      value: `
        <script>
          import ProductCard from './ProductCard.svelte';
        </script>
        <ProductCard
          title="Casque audio bluetooth"
          description="Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident."
          link="#"
          image="/public/produtc_img.jpg"
          price="78"
          color="#ffc239"
        />`
      },{
        label:'ProductCard.svelte',
        value: `
        <script>
          export let image;
          export let title;
          export let description;
          export let link;
          export let price;
          export let color;
        </script>

        <section class="productCard">


          // <div class="productCard_img">
            <img src={image} alt="Image produits" />
          </div>

          <div class="productCard_infos">
            <h2>{title}</h2>
            <p>{description}</p>
            <div class="productCard_row">
              <a href={link} style={'--colorBtn: '}>Voir plus</a>
              <span>{price}$</span>
            </div>
          </div>
        </section>

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
