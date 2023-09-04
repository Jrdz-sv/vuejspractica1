<template>
  <div>
    <h1 class="title">Login</h1>
    <div class="login-form">
      <label for="username" class="label">Usuario</label>
      <input v-model="username" type="text" id="username" class="input" />

      <label for="password" class="label">Contraseña</label>
      <input v-model="password" type="password" id="password" class="input" />

      <button @click="login" class="login-button">Ingresar</button>
    </div>

    <h1 class="title">Nombres</h1>
    <ul v-if="isLoggedIn" class="name-list">
      <li v-for="name in names" :key="name" class="name">{{ name }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "LoginComponent",
  data() {
    return {
      username: "",
      password: "",
      isLoggedIn: false,
      names: ["Kross", "CR7", "Puskas", "Ramos", "Maldini"],
    };
  },
  methods: {
    login() {
      if (this.username === "adminItca" && this.password === "Itca123!") {
        this.isLoggedIn = true;
      }
    },
  },
};
</script>

<style scoped>
.title {
  font-size: 24px;
  margin-bottom: 20px;
}

.login-form {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.label {
  font-size: 16px;
  margin-bottom: 5px;
}

.input {
  padding: 8px;
  font-size: 14px;
  border: 1px solid #ccc;
  border-radius: 4px;
  margin-bottom: 10px;
  width: 200px;
}

.login-button {
  background-color: #007bff;
  color: #fff;
  border: none;
  padding: 10px 20px;
  border-radius: 4px;
  cursor: pointer;
  font-size: 16px;
}

.login-button:hover {
  background-color: #0056b3;
}

.name-list {
  list-style: none;
  padding: 0;
}

.name {
  font-size: 16px;
  margin-bottom: 5px;
}
</style>