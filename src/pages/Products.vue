<template>
  <div>
    <div class="shopping-banner">Selamat Berbelanja!</div>
    <div class="product-grid">
      <div class="product-card" v-for="product in products" :key="product.id">
        <div class="product-image">
          <img :src="product.image" :alt="product.name" />
        </div>
        <div class="product-info">
          <div class="product-name">{{ product.name }}</div>
          <div class="product-price">{{ product.price }}</div>
          <button @click="addToCart(product)">Add to Cart</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      products: [
        { id: 1, name: 'Rose Bouquet', price: 'Rp.150.000', image: '/images/mawar.png' },
        { id: 2, name: 'Sunflower Bouquet', price: 'Rp.79.000', image: '/images/matahari.png' },
        { id: 3, name: 'Tulip Bouquet', price: 'Rp.32.000', image: '/images/tulip.png' },
        { id: 4, name: 'Lily Bouquet', price: 'Rp.40.000', image: '/images/lily.png' },
        { id: 5, name: 'Orchid Bouquet', price: 'Rp.50.000', image: '/images/orchid.png' },
        { id: 6, name: 'Daisy Bouquet', price: 'Rp.60.000', image: '/images/daisy.png' },
        { id: 7, name: 'Carnation Bouquet', price: 'Rp.70.000', image: '/images/carnation.png' },
        { id: 8, name: 'Hydrangea Bouquet', price: 'Rp.80.000', image: '/images/hydrangea.png' },
        { id: 9, name: 'Peony Bouquet', price: 'Rp.90.000', image: '/images/peony.png' },
        { id: 10, name: 'Lavender Bouquet', price: 'Rp.100.000', image: '/images/lavender.png' },
      ]
    };
  },
  methods: {
    addToCart(product) {
      this.$emit('add-to-cart', product);
    },
  }
}
</script>

<style scoped>
.product-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.product-card {
  width: 300px;
  margin: 20px;
  padding: 20px;
  background-color: antiquewhite;
  border: 1px solid #ddd;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.product-card:hover {
  transform: translateY(-5px);
}

.product-image img {
  width: 100%;
  height: auto;
}

.product-info {
  text-align: center;
}

.product-name {
  font-size: 18px;
  font-weight: bold;
  margin: 10px 0;
}

.product-price {
  font-size: 16px;
  color: #ff6b81;
}

button {
  background-color: #55efc4;
  color: #2d3436;
  border: none;
  padding: 10px 20px;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #00b894;
}

.shopping-banner {
  font-size: 32px;
  font-weight: bold;
  text-align: center;
  color: #2d3436;
  padding: 20px;
  margin-bottom: 10px; /* Menurunkan posisi banner sedikit */
}
</style>

<style>
body {
  background-color: #99d9cd; /* Warna abu-abu untuk latar belakang body */
  margin: 0;
  font-family: Arial, sans-serif;
}
</style>
