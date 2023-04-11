<script lang='ts'>
    import { onMount, tick } from "svelte";
    import TickerEven from "./tickerEven.svelte";
    import TickerOdd from "./tickerOdd.svelte";

    export let rain: any; 

    let rainContainer: any;
    let cloudContainer: any;
    let clearContainer: any;
    let lightRainContainer: any;

    function tickerSpacing() {
        window.addEventListener(('resize'), () => {
            const timelineDiv: any = document.getElementById("timeline")
            const width = timelineDiv.offsetWidth;
            console.log('width', width)
            
            const spacing = (width / 24).toFixed(2)

            const ticker = document.querySelectorAll("div.ticker") as NodeListOf<HTMLElement>
            ticker.forEach((d) => {
                d.style.marginRight = `${spacing}px`
            })

        }, true)

    }

    onMount(() => {
        const child = document.createElement('div');
        child.textContent = rain
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

        tickerSpacing()
    })

</script>

<div>
    <h1 class="text-xl"> This is the chart component </h1>
    <div class="flex flex-col">
        <div id="timeline" class="h-11 w-full flex">
            <div bind:this={rainContainer} class="bg-blue-500 justify-center w-1/4 rounded-l-lg flex items-center"></div>
            <div bind:this={cloudContainer} class="bg-slate-300 justify-center w-1/4 flex items-center"></div>
            <div bind:this={clearContainer} class="bg-slate-100 justify-center w-1/4 flex items-center"></div>
            <div bind:this={lightRainContainer} class="bg-blue-400 justify-center w-1/4 rounded-r-lg flex items-center"></div>
        </div>
        <div class="m-0 w-full">
            <div class="ticker w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[10px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
            <div class="ticker w-0.5 inline-block h-[14px] self-stretch bg-black opacity-100 dark:opacity-50 align-top"></div>
        </div>
        <!-- <div class="m-0 flex-row flex">
            <div class="mr-[1.5em] align-top text-[14px]"> 12am </div>
            <div class="mr-[2.5em] align-top text-center text-[14px]"> 2am </div>
            <div class="mr-[2.5em] align-top text-center text-[14px]"> 4am </div>
            <div class="mr-[2.5em] align-top text-center text-[14px]"> 6am </div>
            <div class="mr-[2.5em] align-top text-center text-[14px]"> 8am </div>
            <div class="mr-[2.5em] align-top text-center text-[14px]"> 10am </div>
            <div class="mr-[2.5em] align-top text-center text-[14px]"> 12pm </div>
            <div class="mr-[2.5em] align-top text-center text-[14px]"> 2pm </div>
            <div class="mr-[2.5em] align-top text-center text-[14px]"> 4pm </div>
            <div class="mr-[2.5em] align-top text-center text-[14px]"> 6pm </div>
            <div class="mr-[2.5em] align-top text-center text-[14px]"> 8pm </div>
            <div class="mr-[2.5em] align-top text-center text-[14px]"> 10pm </div>
        </div> -->
        <div> Temp </div>
    </div>
</div>

<style>

</style>