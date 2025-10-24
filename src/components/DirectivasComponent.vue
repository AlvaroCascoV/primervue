<template>
	<div>
		<h1>Ejemplo Directivas</h1>
		<h3>{{ $data }}</h3>

		<label>Introduzca serie:</label>
		<input type="text" v-model="serieNueva" />
		<button v-on:click="nuevaSerie()">Nueva serie??</button>

		<ul v-if="series.length > 0">
			<li v-for="serie in series" :key="serie">{{ serie }}</li>
		</ul>

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
				series: ["Futurama", "Mindhunter", "The Boys", "Stranger Things"],
				numero: 0,
				nombre: "Alumno",
				serieNueva: "",
			};
		},
		methods: {
			nuevaSerie() {
				this.series.push(this.serieNueva);
			},
		},
	};
</script>
