<script lang="ts">
    import Chart from "../components/chart.svelte";
    import "../app.css"

    const data: { day: string, Cloud: number, Rain: number, Clear: Number }[] = [
        { day: "Tuesday", Rain: 4, Cloud: 3, Clear: 1 }
    ]
    
</script>

<div class="mx-[45rem]">
    <Chart/>
</div>


