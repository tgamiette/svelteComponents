<script>
    let isActive = false

    const check = () => {
        isActive = !isActive;
    };

</script>

<form>
    <input type="checkbox" id="confirm" name="confirm" on:click={ check }>
    <label for="confirm">J'accepte les termes et les conditions !</label>
</form>