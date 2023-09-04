<template>
  <div class="container">
    <h1>Ejercicio 1</h1>
    <!--  Mostramos el components-->
    <Card
      :image="require('./assets/play.png')"
      title="PS5"
      sitio="https://www.playstation.com/en-us/"
    />
    <Card
      :image="require('./assets/xbox.png')"
      title="Xbox"
      sitio="https://www.xbox.com/en-US/"
    />
    <Card
      :image="require('./assets/nintendo.png')"
      title="Nintendo"
      sitio="https://www.nintendo.com/"
    />
  </div>

  <div class="container">
    <h1>Ejercicio 2</h1>
    <Age /><hr>
    <Login /><hr>
    <Product /><hr>
  </div>

  <div class="container">
    <h1>Ejercicio 3</h1>
    <Heroe/><hr>
    <Player/><hr>
    <Language/><hr>

  </div>
</template>

<script>
import Card from "./components/CardComponent.vue";
import Age from "./components/AgeComponent.vue";
import Login from "./components/LoginComponent.vue";
import Product from "./components/ProductComponent.vue";
import Heroe from "./components/HeroesComponent.vue";
import Player from "./components/PlayersComponent.vue";
import Language from "./components/LanguagesComponent.vue";
export default {
  name: "App",
  components: {
    Card,
    Age,
    Login,
    Product,
    Heroe,
    Player,
    Language,
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
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
