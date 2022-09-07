<script>
    import Calendar from './Calendar.svelte';
    import CodeDisplay from '../CodeDisplay/CodeDisplay.svelte';
  
</script>
  
  <h2>Calendar</h2>
  <section class="calendar">
    <Calendar />   
      <CodeDisplay tabs={[
        {label: 'App.svelte',
        value: `
          <script>
            import Calendar from './Calendar.svelte';
          </script>
          <Calendar />`
        },{
          label:'Calendar.svelte',
          value: `
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
  
          <style>
          </style>
  
          `
        }]} />
  
  
  </section>
  
  <style>
  
    .calendar{
      display: grid;
      grid-template-columns: 1fr 1fr;
      grid-gap: 50px;
      width: 100%;
    }
  
  </style>