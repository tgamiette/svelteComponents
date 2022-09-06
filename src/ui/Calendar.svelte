<script>
	import { onMount } from 'svelte';
	
    let date;
	let now = new Date(), day, month, year;
	
	onMount(()=> {
        day = '' + now.getDate(),
        month = '' + (now.getMonth() + 1),
        year = now.getFullYear();

    if (month.length < 2) 
        month = '0' + month;

    if (day.length < 2) 
        day = '0' + day;

    date = [year, month, day].join('-');
	})

</script>

<p>
    <label>
        <input type=date value={ date }>
    </label>
</p>