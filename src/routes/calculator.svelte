
<script>
	let total = 0;
	let console = "";
	let state = null;
	function resolveState(){
		switch(state){
			case "add":
				total += parseFloat(console);
				console = "0";
				break;
			case "substract":
				total -= parseFloat(console);
				console = "0";
				break;
			case "multiply":
				total *= parseFloat(console);
				console = "0";
				break;
			case "divide":
				total /= parseFloat(console);
				console = "0";
				break;
			default:
				total = parseFloat(console);
				console = "0";
				break;
		}
	}
	function setOperation(operation){
		resolveState();
		state = operation;
	}
	function setValue(value){
		if(console.toString() == "0" || state == "equal"){
			console = "";
		}
		if(state == "equal"){
			state = null;
		}
		if(value == "C"){
			total = 0;
			state = null;
			console = "";
			return;
		}
		console = console + value;
	}
	function equal(){
		resolveState();
		console = total;
		state = "equal";
	}
</script>

<div class="absolute top- left-5 w-76 border-1 shadow-sm p-2.5">
	<input class="w-full p-5 outline-none text-right text-xl"type="text" bind:value={console} readonly="true"/>
	<div class="flex flex-wrap">
		<div class="flex justify-between w-full">
			<button class="w-1/4" on:click={()=>{setOperation('add');}}>
				+
			</button>
			<button class="w-1/4" on:click={()=>{setOperation('substract');}}>
				-
			</button>
			<button class="w-1/4" on:click={()=>{setOperation('multiply');}}>
				&times;
			</button>
			<button class="w-1/4" on:click={()=>{setOperation('divide');}}>
				&divide;
			</button>
		</div>
		<div class="w-3/4">
			<div  class="flex flex-between">
				<button  class="w-1/3" on:click={()=>{setValue(7);}}>
					7
				</button>
				<button class="w-1/3" on:click={()=>{setValue(8);}}>
					8
				</button>
				<button class="w-1/3" on:click={()=>{setValue(9);}}>
					9
				</button>
			</div>
			<div class="flex flex-between">
				<button class="w-1/3" on:click={()=>{setValue(4);}}>
					4
				</button>
				<button class="w-1/3" on:click={()=>{setValue(5);}}>
					5
				</button>
				<button class="w-1/3" on:click={()=>{setValue(6);}}>
					6
				</button>
			</div>
			<div class="flex flex-between">
				<button class="w-1/3" on:click={()=>{setValue(1);}}>
					1
				</button>
				<button class="w-1/3" on:click={()=>{setValue(2);}}>
					2
				</button>
				<button class="w-1/3" on:click={()=>{setValue(3);}}>
					3
				</button>
			</div>
			<div class="flex flex-between">
				<button class="w-1/3" on:click={()=>{setValue(0);}}>
					0
				</button>
				<button class="w-1/3" on:click={()=>{setValue('.');}}>
					.
				</button>
				<button class="w-1/3" on:click={()=>{setValue('C');}}>
					C
				</button>
			</div>
		</div>
		<div class="flex-1">
			<button class="ml-1/20 w-95/100 h-95/100 bg-cyan-500 text-white" on:click={equal}>
				=
			</button>
		</div>
	</div>
</div>