<template>
  <div>
    <label for="edad">Ingresa tu edad: </label>
    <input type="number" id="edad" v-model="edad" @input="verificarEdad" class="input"/>
    <p v-if="esMenorDeEdad">Es mayor de edad</p>
    <p v-else>Es menor de Edad</p>
  </div>
</template>

<script>
export default {
  name: "AgeComponent",
  data() {
    return {
      edad: 0,
      esMenorDeEdad: false,
    };
  },
  methods: {
    verificarEdad() {
      this.esMenorDeEdad = this.edad >= 18;
    },
  },
};
</script>

<style scoped>
label{
    color: blue;
    font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    font-weight: bolder;
}



.input {
  padding: 8px;
  font-size: 14px;
  border: 1px solid #ccc;
  border-radius: 4px;
  margin-bottom: 10px;
  width: 200px;
}
</style>
