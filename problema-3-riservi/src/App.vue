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
			<div v-for="(item, index) in myArray" 
				:key="item.id" 
				:style="{ backgroundColor: index % 2 !== 0 ? '#808080' : 'none', 
						  display: index % 2 === 0 ? 'none' : 'block' }">
				<p>Nombre: {{ item.name }}</p>
				<p>Roles: {{ item.roles.join(', ') }}</p>
			</div>
		</div>
		<div class="btn success" @click="calculaSalida">
			Generar 
		</div>
		<div class="output">
			{{ output }}
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
			myArray: [
			{ id: 1, name: 'Erick', roles: [4, 1, 3] },
            { id: 2, name: 'Cesar', roles: [6, 2] },
            { id: 3, name: 'Carolina', roles: [2, 4, 6] },
            { id: 4, name: 'Alberto', roles: [1, 2] },
            { id: 5, name: 'Katalina', roles: [4, 3] }
			],
            output: "",
		}
	},
	computed:{
		respuesta() {
            return this.myArray.length;
        }
	},
	methods:{
        calculaSalida() {
            this.output = `El total de listado es: ${this.respuesta}`;
        }
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

.btn {
  border: none; 
  color: black; 
  padding: 14px 28px; 
  cursor: pointer; 
  border-radius: 5px; 
}

.success {background-color: white; border: 2px solid #04AA6D;} 
.success:hover {background-color: #46a049; color: white;}

.output {
  margin-top: 15px;
  font-weight: bold;
}

</style>

