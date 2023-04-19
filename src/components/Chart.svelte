<script lang='ts'>
    import { onMount } from "svelte"; 

    export let rain: any; 
    export let temp: any;

    let rainContainer: any;
    let cloudContainer: any;
    let clearContainer: any;
    let lightRainContainer: any;

    function tickerSpacing() {
        window.addEventListener(('resize'), () => {
            const timelineDiv: any = document.getElementById("timeline")
            const width = timelineDiv.offsetWidth;
            const spacing = (width / 24).toFixed(1)
            const ticker = document.querySelectorAll("div.ticker") as NodeListOf<HTMLElement>
            ticker.forEach((d) => {
                d.style.width = `${spacing}px`
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
    <div class="flex flex-col w-full">
        <div id="timeline" class="h-11 w-full flex box-border">
            <div bind:this={rainContainer} class="bg-blue-500 justify-center w-1/4 rounded-l-lg flex items-center"></div>
            <div bind:this={cloudContainer} class="bg-slate-300 justify-center w-1/4 flex items-center"></div>
            <div bind:this={clearContainer} class="bg-slate-100 justify-center w-1/4 flex items-center"></div>
            <div bind:this={lightRainContainer} class="bg-blue-400 justify-center w-1/4 rounded-r-lg flex items-center"></div>
        </div>
        <div class="w-full flex">
            <div class="ticker h-[10px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[15px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[10px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[15px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[10px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[15px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[10px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[15px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[10px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[15px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[10px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[15px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[10px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[15px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[10px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[15px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[10px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[15px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[10px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[15px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[10px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[15px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[10px] border-l-2 border-black inline-block flex-1"></div>
            <div class="ticker h-[15px] border-l-2 border-black inline-block flex-1"></div>
        </div>
        <div class="m-0 flex-row flex w-full">
            <div class="flex-1 align-top text-[14px] mr-[-10px]"> 12am </div>
            <div class="flex-1 align-top text-[14px]"> 2am </div>
            <div class="flex-1 align-top text-[14px]"> 4am </div>
            <div class="flex-1 align-top text-[14px]"> 6am </div>
            <div class="flex-1 align-top text-[14px]"> 8am </div>
            <div class="flex-1 align-top text-[14px]"> 10am </div>
            <div class="flex-1 align-top text-[14px]"> 12pm </div>
            <div class="flex-1 align-top text-[14px] ml-[5px]"> 2pm </div>
            <div class="flex-1 align-top text-[14px] m1-[5px]"> 4pm </div>
            <div class="flex-1 align-top text-[14px] m1-[5px]"> 6pm </div>
            <div class="flex-1 align-top text-[14px] m1-[5px]"> 8pm </div>
            <div class="flex-1 align-top text-[14px] mr-[12px]"> 10pm </div>
        </div>
        <div class="w-full flex flex-row m-0">
            <div class="flex-1 align-top text-[14px] mr-[-10px]"> {temp[0]} <span> &#176 C </span> </div>
            <div class="flex-1 align-top text-[14px]"> {temp[1]} <span> &#176 C </span> </div>
            <div class="flex-1 align-top text-[14px]"> {temp[2]} <span> &#176 C </span> </div>
            <div class="flex-1 align-top text-[14px]"> {temp[3]} <span> &#176 C </span> </div>
            <div class="flex-1 align-top text-[14px]"> {temp[4]} <span> &#176 C </span> </div>
            <div class="flex-1 align-top text-[14px]"> {temp[5]} <span> &#176 C </span> </div>
            <div class="flex-1 align-top text-[14px]"> {temp[6]} <span> &#176 C </span> </div>
            <div class="flex-1 align-top text-[14px] ml-[5px]"> {temp[7]} <span> &#176 C </span> </div>
            <div class="flex-1 align-top text-[14px] m1-[5px]"> {temp[8]} <span> &#176 C </span> </div>
            <div class="flex-1 align-top text-[14px] m1-[5px]"> {temp[9]} <span> &#176 C </span> </div>
            <div class="flex-1 align-top text-[14px] m1-[5px]"> {temp[10]} <span> &#176 C </span> </div>
            <div class="flex-1 align-top text-[14px] mr-[12px]"> {temp[11]} <span> &#176 C </span> </div>
        </div>
    </div>
</div>

<style>

</style>