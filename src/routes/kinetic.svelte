<h1 class="uppercase text-center">Kinetic Energy Calculator</h1>

<div class="flex flex-col w-64">
    <input class="bg-gray-300 rounded-md my-3 p-1" type="text" placeholder="Mass" bind:value={mass} />
    <input class="bg-gray-300 rounded-md my-3 p-1" type="text" placeholder="Velocity" bind:value={velocity} />
</div>

<script>
    let mass;
    let velocity;
    let kineticEnergy; 
    
    $: { //every time mass and velocity changes this runs
        kineticEnergy = (mass*0.5)*(Math.pow(velocity, 2))
    }
</script>

<p>Kinetic Energy: {kineticEnergy}</p>


