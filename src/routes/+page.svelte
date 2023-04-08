<script lang="ts">
    import Chart from "../components/chart.svelte";
    import "../app.css"

    const data: { day: string, summary: string }[] = [
        { day: "Tuesday", summary: "Rain"}
    ]
    
</script>

<div class="xl:mx-[20em] lg:mx-[10em] md:mx-[5em] sm:mx-[3em]">
    <Chart rain={data[0].summary}/>
</div>


