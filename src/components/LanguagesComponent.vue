<template>
  <div class="programming-languages">
    <h1 class="title">Lenguajes de Programación Populares</h1>
    <ul class="languages-list">
      <li v-for="(language, index) in popularLanguages" :key="index" class="language-item">
        {{ language }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      popularLanguages: [
        "JavaScript",
        "Python",
        "Java",
        "C++",
        "Ruby",
      ],
    };
  },
};
</script>

<style scoped>
.programming-languages {
  text-align: center;
  margin: 20px;
}

.title {
  font-size: 24px;
  margin-bottom: 10px;
  color: #333;
}

.languages-list {
  list-style-type: none;
  padding: 0;
  margin: 0;
}

.language-item {
  margin: 10px 0;
  padding: 10px;
  background-color: #007bff;
  color: #fff;
  border-radius: 4px;
  font-size: 18px;
}

</style>
