<h1>Potential Energy Calculator</h1>
<div class="flex flex-col w-64">
    <input class="bg-gray-300 rounded-md my-3 p-1" type="text" placeholder="Height" bind:value={height}/>
    <input class="bg-gray-300 rounded-md my-3 p-1" type="text" placeholder="Mass" bind:value={mass} />
    <input class="bg-gray-300 rounded-md my-3 p-1" type="text" placeholder="Gravity" bind:value={gravity} />
</div>

<script>
    let height;
    let mass;
    let gravity;
    let potentialEnergy;
    $: {//every time height, mass, or gravity changes, it updates
        potentialEnergy = height * mass * gravity
    }    
</script>

<p>Potential Energy: {potentialEnergy}</p>