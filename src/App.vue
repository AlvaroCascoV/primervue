<template>
  <!-- <img alt="Vue logo" src="./assets/images/logo.png" /> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
  <!-- <HolaMundo /> -->
  <!-- <HomeComponent />
  <CineComponent />
  <MusicaComponent /> -->
  <div>
    <h1 style="color: red">Elemento estatico</h1>
    <MenuComponent />
    <hr />
    <router-view />
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
// import HolaMundo from "./components/HolaMundo.vue";
// import HomeComponent from "./components/HomeComponent.vue";
// import CineComponent from "./components/CineComponent.vue";
// import MusicaComponent from "./components/MusicaComponent.vue";
import MenuComponent from "./components/MenuComponent.vue";

export default {
  name: "App",
  components: {
    // HelloWorld,
    // HolaMundo,
    // CineComponent,
    // HomeComponent,
    // MusicaComponent,
    MenuComponent,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
