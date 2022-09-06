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

<button on:click= { Moins } >-</button>
<label>
	<input bind:value={ index }>
</label>
<button on:click={ Plus } >+</button>