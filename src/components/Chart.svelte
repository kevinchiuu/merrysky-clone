<script lang='ts'>
    import { onMount } from "svelte";
    import String from "./string.svelte";

    const data: { day: string, Cloud: number, Rain: number, Clear: Number }[] = [
        { day: "Tuesday", Rain: 4, Cloud: 3, Clear: 1 }
    ]
    
    let rainContainer: any;
    let cloudContainer: any;
    let rainContainer2: any;
    let cloudContainer2: any;

    onMount(() => {
        document.createElement('div');

        const child2 = document.createElement('div');
        child2.textContent = 'Cloud'
        cloudContainer.appendChild(child2)

        const child3 = document.createElement('div');
        child3.textContent = 'Rain'
        rainContainer2.appendChild(child3)

        const child4 = document.createElement('div');
        child4.textContent = 'Cloud'
        cloudContainer2.appendChild(child4)
    })

</script>

<div>
    <h1 class="text-xl"> This is the chart component </h1>
    <!-- <div class="h-14 w-96 flex">
        <div class="bg-blue-500 h-full w-1/4 align-middle text-center rounded-l-lg"> <h1 class="h-full w-full text-center"> Rain </h1> </div>
        <div class="bg-slate-300 h-full w-1/4 text-center"> Cloudy </div>
        <div class="bg-blue-500 h-full w-1/4 text-center"> Rain </div>
        <div class="bg-slate-300 h-full w-1/4 text-center rounded-r-lg"> Cloudy </div>
    </div> -->
    <div class="h-14 w-96 flex">
        <div bind:this={rainContainer} class="bg-blue-500 justify-center text-center w-1/4 rounded-l-lg"> <String string={"Rain"}/> </div>
        <div bind:this={cloudContainer} class="bg-slate-300 justify-center text-center w-1/4"></div>
        <div bind:this={rainContainer2} class="bg-blue-500 justify-center text-center w-1/4"></div>
        <div bind:this={cloudContainer2} class="bg-slate-300 justify-center text-center w-1/4 rounded-r-lg"></div>
    </div>
</div>