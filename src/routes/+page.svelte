<script lang="ts">
    import Chart from "../components/chart.svelte";
    import "../app.css"

    const data: { day: string, summary: string }[] = [
        { day: "Tuesday", summary: "Rain"}
    ]
    
</script>

<div class="mx-[45rem]">
    <Chart rain={data[0].summary}/>
</div>


