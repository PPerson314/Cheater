<script>
    const pages = ["calculator", "cat", "kinetic", "current", "potential", "acdc"]
</script>

<h1 class="text-4xl text-center my-8 uppercase">Home</h1>
<div class="grid gap-4 grid-cols-3">
    {#each pages as page}
        <a class="bg-slate-600 rounded-md uppercase h-20 text-center p-5 m-2 text-lg" href="/{page}">{page}</a>
    {/each}
</div>