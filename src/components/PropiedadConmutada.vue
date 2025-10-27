<template>
	<h1>Propiedades Conmutadas</h1>
	<ul>
		<li v-for="game in juegosRojos" :key="game" v-html="game"></li>
	</ul>
	<ul>
		<li v-for="game in juegos" :key="game">{{ game }}</li>
	</ul>
</template>
<script>
	export default {
		name: "PropiedadConmutada",
		computed: {
			//SE ESCRIBEN COMO UN METODO PERO SE UTILIZA COMO UNA PROPIEDAD
			juegosRojos() {
				var datos = this.juegos;
				var i = 0;
				for (var game of this.juegos) {
					var juegoRojo = "<span style='color:red'>" + game + "</span>";
					datos[i] = juegoRojo;
					i++;
				}
				return datos;
			},
		},
		data() {
			return {
				juegos: ["Parchis", "Canicas", "Luzverde, luz roja", "La galleta"],
			};
		},
	};
</script>
