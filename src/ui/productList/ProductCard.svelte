<script>
  export let image;
  export let title;
  export let description;
  export let link;
  export let price;
  export let color;
</script>

<section class="productCard">
  <div class="productCard_img">
    <img src={image} alt="Image produits" />
  </div>

  <div class="productCard_infos">
    <h2>{title}</h2>
    <p>{description}</p>
    <div class="productCard_row">
      <a href={link} style={`--colorBtn: ${color}`}>Voir plus</a>
      <span>{price}$</span>
    </div>
  </div>
</section>


<style>

 .productCard{
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
   border: 1px solid var(--colorBtn);
   background: var(--colorBtn);
   color: white;
   transition: 0.3s ease-in;
   padding: 10px 20px;
   border-radius: 10px;
 }

 .productCard_row a:hover{
   background: transparent;
   color: var(--colorBtn);
 }

 .productCard_row span{
   font-weight: bold;
   font-size: 1.2rem;
 }

</style>
