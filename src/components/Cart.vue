<template>
  <div class="cart-container">
    <!-- Tombol keranjang untuk membuka dan menutup keranjang -->
    <q-btn class="cart-btn" color="primary" icon="shopping_cart" @click="toggleCart" />
    <!-- Konten keranjang belanja -->
    <q-drawer v-model="showCart" show-if-above side="right" width="300px" v-show="showCart">
      <q-toolbar class="bg-primary text-white">
        <q-toolbar-title>
          <q-icon name="shopping_cart" class="sidebar-icon" />
          Keranjang
        </q-toolbar-title>
        <!-- Tambahkan tombol untuk menutup keranjang belanja -->
        <q-btn flat icon="close" @click="toggleCart" />
      </q-toolbar>
      <q-list>
        <!-- Daftar produk dalam keranjang belanja -->
        <q-item v-for="(item, index) in cartItems" :key="item.id">
          <q-item-section>
            <!-- Tambahkan gambar produk di sini -->
            <img :src="item.image" alt="Product Image" class="product-image">
          </q-item-section>
          <q-item-section>{{ item.name }}</q-item-section>
          <q-item-section side="right">{{ item.price }}</q-item-section>
          <!-- Tombol "Delete" untuk menghapus item -->
          <q-item-section side="right">
            <q-btn flat color="negative" icon="delete" @click="deleteItem(index)" class="delete-btn" />
          </q-item-section>
        </q-item>
      </q-list>
      <!-- Tampilkan total harga belanjaan -->
      <div class="total-price">Total: {{ calculateTotalPrice() }}</div>
      <!-- Tombol checkout -->
      <q-btn class="checkout-btn" color="primary" label="Checkout" @click="checkout" />
    </q-drawer>
  </div>
</template>

<script>
export default {
  props: {
    cartItems: {
      type: Array,
      required: true
    },
    modelValue: {
      type: Boolean,
      required: true
    }
  },
  data() {
    return {
      showCart: false
    };
  },
  methods: {
    toggleCart() {
      // Toggle status tampilan keranjang
      this.showCart = !this.showCart;
    },
    deleteItem(index) {
      // Hapus item dari keranjang belanja berdasarkan indeks
      this.cartItems.splice(index, 1);
    },
    calculateTotalPrice() {
      // Fungsi untuk menghitung total harga belanjaan
      let totalPrice = 0;
      for (let item of this.cartItems) {
        // Harga dari setiap item dijumlahkan
        totalPrice += parseFloat(item.price.replace('Rp.', '').replace(',', ''));
      }
      // Mengembalikan total harga dengan format mata uang dengan dua desimal
      return 'Rp.' + totalPrice.toFixed(3).replace(/\d(?=(\d{3})+\.)/g, '$&,');
    },
    checkout() {
      // Simulasi proses checkout
      alert('Pesanan Anda sedang diproses!');
      // Hapus semua item dari keranjang setelah proses checkout
      this.cartItems.splice(0, this.cartItems.length);
      // Tutup sidebar setelah checkout
      this.toggleCart();
    }
  }
}
</script>

<style scoped>
.cart-container {
  position: relative;
  z-index: 999;
}

/* Gaya untuk tombol keranjang */
.cart-btn {
  position: fixed;
  bottom: 70px;
  /* Sesuaikan dengan posisi yang Anda inginkan */
  right: 20px;
  /* Sesuaikan dengan posisi yang Anda inginkan */
  z-index: 1000;
  border-radius: 50%;
  font-size: 24px;
  width: 60px;
  height: 60px;
  background-color: #FF4081;
  /* Warna latar belakang */
  color: #FFF;
  /* Warna teks */
}

/* Gaya untuk gambar produk */
.product-image {
  width: 50px;
  height: 50px;
  object-fit: cover;
  border-radius: 50%;
  /* Agar gambar terlihat seperti lingkaran */
}

/* Gaya untuk tombol hapus */
.delete-btn {
  color: #FF4081;
  /* Warna ikon hapus */
}

/* Gaya untuk icon di sidebar */
.sidebar-icon {
  font-size: 24px;
  margin-right: 8px;
}

/* Gaya untuk total harga belanjaan */
.total-price {
  font-size: 18px;
  font-weight: bold;
  margin-top: 20px;
  text-align: center;
}

/* Gaya untuk tombol checkout */
.checkout-btn {
  margin-top: 20px;
  width: 100%;
}
</style>
