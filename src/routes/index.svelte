<script>
    const pages = ["calculator", "cat", "kinetic", "current", "potential", "acdc"]
</script>

<div class="bg-[url('/images/download.jpg')] h-96">
    <h1 class="text-4xl text-center my-8 uppercase">Home</h1>
    <div class="grid gap-4 grid-cols-3">
        {#each pages as page}
            <a class="bg-slate-600 rounded-md uppercase h-20 text-center p-5 text-lg" href="/{page}">{page}</a>
        {/each}
    </div>
</div>