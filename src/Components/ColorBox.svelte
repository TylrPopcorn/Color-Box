
<!-- JAVASCRIPT -->
<script>
	let currentColor;
    const colors = [
		"#E53935",	"#E91E63",
		"#9C27B0",	"#673AB7",
		"#3F51B5",	"#2196F3",
		"#03A9F4",	"#00BCD4",
		"#009688",	"#4CAF50",
		"#8BC34A",	"#CDDC39",
		"#FFEB3B",	"#FFC107",
		"#FF9800",	"#FF5722",
	];
	currentColor = colors[Math.floor(Math.random() * colors.length)];

	//------ FUNCTIONS -----\\
	const chooseRandomColor = function(){
		const idx = Math.floor(Math.random() * colors.length);
  		currentColor = colors[idx];
	}
</script>

<!-- HTML -->
<div class="ColorBox" style="background-color: {currentColor};" on:click={chooseRandomColor} on:keypress={()=>{}}></div>

<!-- CSS -->
<style>
    .ColorBox {
        width: 12vw;
        height: 30vh;

		/* In case I put anything in here? */
        display: flex;
        align-items: center;
        justify-content: center;
		
        color: white;
        font-weight: bold;
        border-radius: 5px;
        text-transform: uppercase;
		
    }
</style>