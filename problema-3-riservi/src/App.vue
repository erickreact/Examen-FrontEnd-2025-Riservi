<template>
<html>
	<head>
	</head>
	<body>
		<div id="contenedor">
			<div class="bloque1">
				<p>Este es el Bloque 1 dentro del contenedor.</p>
			</div>
			<div class="bloque2">
				<p>Este es el contenido del Bloque 2 dentro del contenedor, este contiene mas texto, por eso debe ser mas largo.</p>
			</div>
			<div class="clear"></div>
		</div>
		<div class="bloque1">
			<p>Este es el Bloque 1 fuera del contenedor.</p>
		</div>
		<div class="bloque2">
			<p>Este es el Bloque 2 fuera del contenedor.</p>
		</div>
		<div class="v-container">

		</div>
		<div class="btn">
			Generar
		</div>
		<div class="output">
		</div>
	</body>
</html>
</template>
<script>
export default {

	name: 'SupportView',
	components: {

	},
	data () {
		return {
			myArray: [],
			output:"",
			
		}
	},
	computed:{
	
	},
	methods:{

	}
}
</script>
<style type="text/css">

body {
    text-align: center;
}

#contenedor {
    width: 600px;
    margin: 0 auto;
    padding: 10px;
    border: 1px dashed gray;
    margin-bottom: 10px;
}

#contenedor .bloque1 {
    width: 100px;
    margin-top: 70px;
    float: left;
	margin: 5px;
    background-color: red;
    color: #F5F5DC;
}

#contenedor .bloque2 {
    width: 100px;
    float: left;
    margin: 5px;
    background-color: yellow;
    color: black;
}

#contenedor .bloque1 p {
    font-style: italic;
}

.bloque2 p {
  font-weight: bold;
}

.bloque1 {
    background-color: red;
    color: #F5F5DC;
}

.bloque2 {
    background-color: yellow;
    color: black;
}

p {
  padding: 10px;
}

.clear {
    clear: both;
}

</style>

