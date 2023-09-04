<template>
  <div class="product-container">
    <h1 class="title">Productos</h1>
    <label for="categorySelect" class="label">Selecciona la categoría:</label>
    <select v-model="selectedCategory" id="categorySelect" class="select">
      <option value="A">Categoria A</option>
      <option value="B">Categoria B</option>
      <option value="C">Categoria C</option>
    </select>

    <h2 class="subtitle">Productos en la categoría {{ selectedCategory }}</h2>
    <div class="product-grid">
      <div v-for="product in filteredProducts" :key="product.id" class="product-item">
        {{ product.name }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductComponent",
  data() {
    return {
      selectedCategory: "A",
      products: [
        { id: 1, name: "Lamborguini Aventador", category: "A" },
        { id: 2, name: "Toyota Supra", category: "B" },
        { id: 2, name: "Toyota E480", category: "B" },
        { id: 2, name: "Toyota GTO", category: "B" },
        { id: 3, name: "Lamborguini Evo", category: "A" },
        { id: 3, name: "Lamborguini Centenario", category: "A" },
        { id: 4, name: "Ferrari Spider", category: "C" },
        { id: 4, name: "La Ferrari", category: "C" },
        { id: 4, name: "Ferrari Enzo", category: "C" },
      ],
    };
  },
  computed: {
    filteredProducts() {
      return this.products.filter(
        (product) => product.category === this.selectedCategory
      );
    },
  },
};
</script>

<style scoped>
.product-container {
  text-align: center;
  margin: 20px;
}

.title {
  font-size: 24px;
  margin-bottom: 10px;
}

.label {
  font-size: 20px;
  margin-right: 10px;
}

.select {
  font-size: 16px;
  padding: 5px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

.subtitle {
  font-size: 20px;
  margin-top: 20px;
}

.product-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  grid-gap: 10px;
  justify-items: center;
}

.product-item {
  font-size: 18px;
  border: 1px solid #ccc;
  padding: 10px;
  border-radius: 4px;
  background-color: aqua;
}
</style>