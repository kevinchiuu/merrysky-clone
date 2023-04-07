<script lang='ts'>
    import { onMount } from "svelte";

    const data: { day: string, Cloud: number, Rain: number, Clear: Number }[] = [
        { day: "Tuesday", Rain: 4, Cloud: 3, Clear: 1 }
    ]
    
    let rainContainer: any;
    let cloudContainer: any;
    let clearContainer: any;
    let lightRainContainer: any;

    onMount(() => {
        const child = document.createElement('div');
        child.textContent = 'Rain'
        rainContainer.appendChild(child)

        const child2 = document.createElement('div');
        child2.textContent = 'Cloud'
        cloudContainer.appendChild(child2)

        const child3 = document.createElement('div');
        child3.textContent = 'Clear'
        clearContainer.appendChild(child3)

        const child4 = document.createElement('div');
        child4.textContent = 'Light Rain'
        lightRainContainer.appendChild(child4)
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
    <div class="flex flex-col">
        <div class="h-11 w-full flex">
            <div bind:this={rainContainer} class="bg-blue-500 justify-center w-1/4 rounded-l-lg flex items-center"></div>
            <div bind:this={cloudContainer} class="bg-slate-300 justify-center w-1/4 flex items-center"></div>
            <div bind:this={clearContainer} class="bg-slate-100 justify-center w-1/4 flex items-center"></div>
            <div bind:this={lightRainContainer} class="bg-blue-400 justify-center w-1/4 rounded-r-lg flex items-center"></div>
        </div>
        <div class="m-0 w-full">
            <div class="w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
            <div class="w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 mr-[1.65em] align-top"></div>
        </div>
        <div class="m-0 flex-row flex">
            <div class="mr-[1.5em] align-top text-[14px]"> 12am </div>
            <div class="mr-[2em] align-top text-center text-[14px]"> 2am </div>
            <div class="mr-[2em] align-top text-center text-[14px]"> 4am </div>
            <div class="mr-[2em] align-top text-center text-[14px]"> 6am </div>
            <div class="mr-[2em] align-top text-center text-[14px]"> 8am </div>
            <div class="mr-[2em] align-top text-center text-[14px]"> 10am </div>
            <div class="mr-[2em] align-top text-center text-[14px]"> 12pm </div>
            <div class="mr-[2em] align-top text-center text-[14px]"> 2pm </div>
            <div class="mr-[2.5em] align-top text-center text-[14px]"> 4pm </div>
            <div class="mr-[2.5em] align-top text-center text-[14px]"> 6pm </div>
            <div class="mr-[2.5em] align-top text-center text-[14px]"> 8pm </div>
            <div class="mr-[2.5em] align-top text-center text-[14px]"> 10pm </div>
        </div>
        <div> Temp </div>
    </div>
</div>