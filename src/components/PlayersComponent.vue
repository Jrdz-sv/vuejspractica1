<template>
  <div class="football-players">
    <h1 class="title">Jugadores de Fútbol</h1>
    <ul class="players-list">
      <li
        v-for="(jugador, index) in jugadores"
        :key="index"
        class="player-item"
      >
        <div class="player-info">
          <strong class="player-label">Nombre:</strong>
          <span class="player-name">{{ jugador.nombre }}</span>
        </div>
        <div class="player-info">
          <strong class="player-label">Equipo:</strong>
          <span class="player-team">{{ jugador.equipo }}</span>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "PlayerComponent",
  data() {
    return {
      jugadores: [
        { nombre: "Luka Modric", equipo: "Real Madrid" },
        { nombre: "Toni Kross", equipo: "Real Madrid" },
        { nombre: "Vini Jr", equipo: "Real Madrid" },
        { nombre: "Lionel Messi", equipo: "Inter Miami" },
        { nombre: "Cristiano Ronaldo", equipo: "AllNasar" },
        { nombre: "Kylian Mbappé", equipo: "Paris Saint-Germain" },
        { nombre: "Robert Lewandowski", equipo: "Barca" },
        { nombre: "Kevin De Bruyne", equipo: "Manchester City" },
        { nombre: "Erling Haaland", equipo: "Manchester City" },
        { nombre: "Mohamed Salah", equipo: "Liverpool" },
      ],
    };
  },
};
</script>

<style scoped>
.football-players {
  text-align: center;
  margin: 20px;
}

.title {
  font-size: 24px;
  margin-bottom: 10px;
}

.players-list {
  list-style-type: none;
  padding: 0;
  margin: 0;
}

.player-item {
  margin: 10px 0;
  padding: 10px;
  background-color: rgb(57, 236, 57);
  border: 1px solid #ccc;
  border-radius: 4px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.player-label {
  font-weight: bold;
  margin-right: 10px;
}

.player-info {
  display: flex;
  align-items: center;
}

.player-name {
  font-size: 16px;
}

.player-team {
  font-size: 16px;
}
</style>
