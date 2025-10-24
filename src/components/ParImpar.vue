<template>
	<div>
		<h1>Par Impar</h1>
		<h2 v-if="numero % 2 == 0">Par</h2>
		<h2 v-else>Impar</h2>
		<label>Introduce Numero:</label>
		<input type="number" v-model="numero" />
		<button v-on:click="numeroAleatorio()">Random</button>
	</div>
</template>
<script>
	export default {
		name: "ParImpar",
		data() {
			return {
				numero: 0,
			};
		},
		methods: {
			numeroAleatorio() {
				this.numero = Math.floor(Math.random() * 100) + 1;
			},
		},
	};
</script>
