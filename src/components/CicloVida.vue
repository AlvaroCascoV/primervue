<template>
	<div>
		<h1>Ciclo vida y métodos VUE</h1>
		<h2 style="color: red">{{ mensaje }}</h2>
		<button @click="cambiarMensaje()">Cambiar mensaje</button>
	</div>
</template>
<script>
	export default {
		name: "CicloVida",
		data() {
			return {
				mensaje: "Hoy es viernes!!",
			};
		},
		methods: {
			//AQUI INCLUIMOS NUESTROS METODOS PERSONALIZADOS
			cambiarMensaje() {
				//PARA ACCEDER A LAS VARIABLES data() DEL COMPONENT
				//DEBEMOS UTILIZAR LA PALABRA this
				this.mensaje = "Hoy se sale!!";
			},
		},
		mounted() {
			console.log("Component mounted");
		},
		created() {
			console.log("Component created");
		},
		updated() {
			console.log("Component updated");
		},
		unmounted() {
			console.log("Component unmounted");
		},
	};
</script>
