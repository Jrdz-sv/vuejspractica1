<template>
  <h1 class="title">Superhéroes y sus Superpoderes</h1>
  <div class="superheroes-container">
    <ul class="superheroes-list">
      <li
        v-for="(superpower, superhero) in superheroes"
        :key="superhero"
        class="superhero-item"
      >
        <strong class="superhero-name">{{ superhero }}:</strong>
        <span class="superpower">{{ superpower }}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HeroesComponent",
  data() {
    return {
      superheroes: {
        Superman: "Super fuerza",
        Batman: "Inteligencia",
        "Spider-Man": "Sentido arácnido",
        "Wonder Woman": "Fuerza divina",
        "Iron Man": "Tecnología avanzada",
      },
    };
  },
};
</script>

<style scoped>
.superheroes-container {
  text-align: center;
  margin: 20px;
}

.title {
  font-size: 24px;
  margin-bottom: 10px;
}

.superheroes-list {
  list-style-type: none;
  padding: 0;
  margin: 0;
}

.superhero-item {
  margin-bottom: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
  padding: 10px;
  background-color: rgb(183, 232, 8);
}

.superhero-name {
  font-weight: bold;
}

.superpower {
  margin-left: 05px;
}
</style>
