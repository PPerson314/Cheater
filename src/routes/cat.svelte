<h1>Cat ometer </h1>

<div class="flex flex-col w-64">
    <input class="bg-gray-300 rounded-md my-3 mx-2 p-1" type="text" placeholder="big cat" bind:value={bigcat} />
    <input class="bg-gray-300 rounded-md my-3 mx-2 p-1" type="text" placeholder="fast cat" bind:value={FastCat} />
</div>

<script>
    let bigcat;
    let FastCat;
    let DaCat; 
    let src = "/images/cat.png"
    
    $: { //every time mass and velocity changes this runs
        DaCat = (bigcat*0.5)*(Math.pow(FastCat, 2))
    }
</script>

<img {src} alt="hi" />
<p>Cat Energy Energy: {DaCat}</p>
