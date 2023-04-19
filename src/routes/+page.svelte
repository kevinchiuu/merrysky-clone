<script lang="ts">
    import Chart from "../components/chart.svelte";
    import "../app.css"

    const data: { day: string, summary: string, temp: Number[] }[] = [
        { day: "Tuesday", summary: "Rain", temp:[1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12]}
    ]
    
</script>

<div class="xl:mx-[20em] lg:mx-[10em] md:mx-[5em] sm:mx-[3em]">
    <Chart rain={data[0].summary} temp={data[0].temp}/>
</div>


