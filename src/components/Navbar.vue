<template>
  <q-header class="bg-pastel-blue">
    <div class="container">
      <q-toolbar>
        <q-toolbar-title class="youtube-font">
          <span class="highlight text-black">Ivony</span><span class="highlight text-white">Shop</span>
        </q-toolbar-title>
        <div class="nav-links">
          <q-btn flat class="nav-btn" to="/" color="pastel-pink" @mouseover.native="$emit('toggle-cart')" @mouseleave.native="$emit('close-cart')">Home</q-btn>
          <q-btn flat class="nav-btn" to="/products" color="pastel-pink" @mouseover.native="$emit('toggle-cart')" @mouseleave.native="$emit('close-cart')">Products</q-btn>
          <q-btn flat class="nav-btn" to="/about" color="pastel-pink" @mouseover.native="$emit('toggle-cart')" @mouseleave.native="$emit('close-cart')">About</q-btn>
          <q-btn flat class="nav-btn" to="/contact" color="pastel-pink" @mouseover.native="$emit('toggle-cart')" @mouseleave.native="$emit('close-cart')">Contact</q-btn>
        </div>
      </q-toolbar>
    </div>
  </q-header>
</template>

<script>
export default {}
</script>

<style scoped>
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px 50px;
}

.nav-btn {
  color: #fff;
  font-weight: bold;
  background-color: #ff6b8124;
  border: none;
  border-radius: 25px;
  padding: 10px 20px;
  margin: 0 15px;
  transition: background-color 0.3s, color 0.3s;
}

.nav-btn:hover {
  background-color: #d5e4e6;
}

.bg-pastel-blue {
  background-color: #00bcd4;
}

.highlight {
  padding: 5px 10px;
  border-radius: 5px;
}

.text-black {
  background-color: #ffd700; /* Warna latar belakang kuning */
  color: #000; /* Warna teks hitam */
}

.text-white {
  background-color: #000; /* Warna latar belakang hitam */
  color: #fff; /* Warna teks putih */
}

.youtube-font {
  font-family: 'Roboto', sans-serif;
  font-size: 28px;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  font-weight: bold;
}

.nav-links {
  display: flex;
  align-items: center;
  justify-content: flex-end;
}

.nav-links .nav-btn:last-child {
  margin-right: 0;
}
</style>
