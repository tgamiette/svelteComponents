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