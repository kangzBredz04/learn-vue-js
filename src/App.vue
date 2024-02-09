<template>
  <div>
    <h1>Welcome to {{ name }}</h1>
    <button @click="changeName">Ganti Nama</button>
  </div>
  <div><a :href="url">URL</a></div>
  <div>
    <input type="text" v-model="inputName" />
    <h3>Hasil inputan : {{ inputName }}</h3>
  </div>
  <div v-if="products.length">
    <ol>
      <li v-for="item in products" :key="item.id">
        {{ item.nameProduct }} - {{ item.priceProduct }}
      </li>
    </ol>
  </div>
  <div v-else><h3>Data tidak ditemukan</h3></div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "Wahyu",
      url: "https://vuejs.org/",
      inputName: "",
      products: [
        { id: 1, nameProduct: "Product 1", priceProduct: 1000 },
        { id: 2, nameProduct: "Product 2", priceProduct: 2000 },
        { id: 3, nameProduct: "Product 3", priceProduct: 3000 },
        { id: 4, nameProduct: "Product 4", priceProduct: 4000 },
        { id: 5, nameProduct: "Product 5", priceProduct: 5000 },
      ],
    };
  },
  methods: {
    changeName() {
      this.name = "Jebredz";
    },
  },
};
</script>
