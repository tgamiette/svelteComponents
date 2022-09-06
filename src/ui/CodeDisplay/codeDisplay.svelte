
<script>
  export let tabs = [];
  let activeTabValue = 0;
  const handleClick = (index) => {
    activeTabValue = index;
    activeTabValue = activeTabValue;
  };
</script>



<div class="productCard_code">
  <nav>
    <ul>
      {#each tabs as tab, index}
        <li>
          <span on:click={() => handleClick(index)} class={activeTabValue === index ? "hello" : ''}>{tab.label}</span>
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


<style>
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
