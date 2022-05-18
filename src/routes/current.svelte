
<script>
    import {slide} from 'svelte/transiton'
    let volts;
    let ohms;
    let amps;
    let current;

    $: {
        if (volts===undefined||volts==="") {
            current = ohms*amps
        } else if (ohms===undefined||ohms==="") {
            current = volts/amps
        } else if (amps===undefined||amps==="") {
            current = volts/ohms
        }
    }
</script>

<div transition:slide>
    <h1 class="uppercase text-center text-2xl">Current Calculator</h1>
    
    <div class="flex flex-col w-64">
        <input class="bg-gray-300 rounded-md my-3 p-1 mx-2 shadow-md shadow-slate-400 hover:shadow-lg" type="text" placeholder="Volts" bind:value={volts} />
        <input class="bg-gray-300 rounded-md my-3 p-1 mx-2 shadow-md shadow-slate-400 hover:shadow-lg" type="text" placeholder="Ohms" bind:value={ohms} />
        <input class="bg-gray-300 rounded-md my-3 p-1 mx-2 shadow-md shadow-slate-400 hover:shadow-lg" type="text" placeholder="Amps" bind:value={amps} />
    </div>
    <p>Result: {current}</p>
</div>