<script lang="ts">
    let data = [1, 2, 3, 4, 5]
</script>

<div>
    <h1> This is the strip graph </h1>
    {#each data as data, index}
    <div class="flex-row md:contents">
        <div class="col-start-2 col-end-4 mr-10 md:mx-auto relative">
          <div class="h-full w-6 flex items-center justify-center">
            <div class="h-full w-1 bg-green-500 pointer-events-none"></div>
          </div>
        </div>
        <div class="bg-green-500 col-start-4 col-end-12 p-4 rounded-xl my-4 mr-auto shadow-md w-full">
          <h3 class="font-semibold text-lg mb-1"> {data} </h3>
        </div>
      </div>
    {/each}
</div>