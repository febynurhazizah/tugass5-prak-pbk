<template>
  <q-layout view="hHh lpR fFf">
    <!-- Navbar -->
    <Navbar @toggle-cart="toggleCart" />

    <!-- Page Content -->
    <q-page-container>
      <router-view @add-to-cart="addToCart" />
    </q-page-container>

    <!-- Cart -->
    <Cart :cart-items="cartItems" v-model="showCart" />

    <!-- Footer -->
    <Footer />
  </q-layout>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'
import Cart from './components/Cart.vue'

export default {
  components: {
    Navbar,
    Footer,
    Cart
  },
  data() {
    return {
      cartItems: [], 
      showCart: false, // Properti untuk mengontrol status tampilan keranjang
      showCartButton: true 
    };
  },
  methods: {
    addToCart(product) {
      this.cartItems.push(product);
    },
    toggleCart() {
      // Toggle status tampilan keranjang
      this.showCart = !this.showCart;
    }
  }
}
</script>

<style>
.cart-button {
  position: fixed;
  bottom: 20px;
  right: 20px;
  z-index: 999;
}
</style>
