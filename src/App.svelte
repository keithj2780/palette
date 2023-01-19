<script>
	//	https://github.com/keithj2780/svelte-editable-palette
	import HSVColourPicker from './HSVColourPicker.svelte';
	import ColourPicker from './ColourPicker.svelte';
	
	function colorChange(e) {
		console.log('change',e.detail);
	}
	function colorInput(e) {
		console.log('input',e.detail);
	}
</script>

<h1>HSV Colour Picker</h1>

<HSVColourPicker startColor={"#000000"} on:change={colorChange} on:input={colorInput} showAlphaSlider={true}
    showInfoBox={true}/>


<h1>Palette editable using HSV Colour Picker</h1>

<ColourPicker on:input={colorInput}/>
