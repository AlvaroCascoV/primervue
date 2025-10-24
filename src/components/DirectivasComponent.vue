<template>
	<div>
		<h1>Ejemplo Directivas</h1>
		<h3>{{ $data }}</h3>
		<label>Introduzca un número</label>
		<input type="number" v-model="numero" />
		<h3 v-if="numero > 0" style="color: green">POSITIVO</h3>
		<h3 v-else-if="numero < 0" style="color: red">NEGATIVO</h3>
		<h3 v-else style="color: darkblue">CERO</h3>
	</div>
</template>
<script>
	export default {
		name: "DirectivasComponent",
		data() {
			return {
				numero: 0,
				nombre: "Alumno",
			};
		},
	};
</script>
