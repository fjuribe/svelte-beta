<script>
	import Componente from './component/Componente.svelte';
	let name = 'Dragon ball z';
	let src='https://dragon-ball-api.herokuapp.com/images/Vegeta.jpg';
	let string="<h1>hola</h2>";

    let count=0;
	function presionar(){
		count+=1;
	}
</script>


<style>
  div{
  	text-align: center
  }
  p{
   color:purple;
   font-family:'Comic Sans MS',cursive;
   font-size:2em;
  }
</style>


<div>
<h1>{name.toUpperCase()}</h1>
<figure>
	<Componente/>
	<img src={src} alt="Es una imagen" width="200" height="370">
	<figcaption>explanatory caption</figcaption>
	<p>{count} {count===1 ?'time':'times'}</p>	
</figure>

<button on:click={presionar}>
	presionar 
</button>
<!-- <p>{@html string}</p> -->
</div>
