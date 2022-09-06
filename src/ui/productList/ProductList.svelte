<script>
  import ProductCard from './ProductCard.svelte';

  let tabs = [
    {label: 'App.svelte',
    value: `
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
      <section class="productCard">
        <div class="productCard_img">
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
    }
  ]

  let activeTabValue = 0;
  const handleClick = (index) => {
    activeTabValue = index;
    activeTabValue = activeTabValue;
  };
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

    <div class="productCard_code">
      <nav>
        <ul>
          {#each tabs as tab, index}
            <li>
              <span on:click={() => handleClick(index)}>{tab.label}</span>
            </li>
          {/each}
        </ul>
      </nav>
      <pre>
        {#each tabs as tab, index}
          {#if activeTabValue === index}
            <code class="codeScetion">{tab.value}</code>
          {/if}
        {/each}
      </pre>
    </div>

</section>

<style>

  .productCard{
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 50px;
    width: 100%;
  }

  .codeScetion{
    width: 50%;
    overflow: scroll;
  }
  nav{
    margin: 0;
    display: flex;
    flex-direction: row;
    align-items: flex-start;
  }

  nav ul {
    display: flex;
    flex-direction: row;
    list-style: none;
    padding: 0;
    margin: 0;
  }
  nav li {
    margin: 0 20px 0 0;
    padding: 10px 20px;
    border-radius: 10px 10px 0 0;
    background: #383838;
    color: #ffb72a50;
    cursor: pointer;
  }

  nav li .active{
    color: #ffb72a;
    font-weight: bold;
  }

  pre{
    height: 70vh;
    background: #383838;
    padding: 20px 0px;
    margin: 0;
    color: white;
    text-align: left;
    width: 50vw;
    overflow: scroll;
  }

</style>
