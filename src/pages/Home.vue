<template>
  <div class="home-page">
    <h1>Selamat Datang di Ivony Shop</h1>
    <p>Temukan keindahan alam dengan koleksi bunga kami yang menakjubkan!</p>

    <div class="q-pa-md">
      <q-carousel
        animated
        v-model="slide"
        arrows
        navigation
        infinite
      >
        <q-carousel-slide :name="1" img-src="https://goldenfarm99.com/wp-content/uploads/2023/10/gambar-bunga-mawar-dengan-latar-belakang-hitam-768x439.jpg" />
        <q-carousel-slide :name="2" img-src="https://cdn0-production-images-kly.akamaized.net/Ock34Un1NAvTtZkr0FUkquvMzJU=/1280x720/smart/filters:quality(75):strip_icc():format(webp)/kly-media-production/medias/3231474/original/092645800_1599532012-brianne-reed-5fKVGNg4QaM-unsplash.jpg" />
        <q-carousel-slide :name="3" img-src="https://goldenfarm99.com/wp-content/uploads/2023/10/gambar-bunga-aesthetic-kartun.jpg" />
        <q-carousel-slide :name="4" img-src="https://e1.pxfuel.com/desktop-wallpaper/267/380/desktop-wallpaper-pink-flowers-aesthetic-laptop-flower-aesthetics.jpg" />
      </q-carousel>
    </div>

    <p>Kunjungi product kami untuk melihat koleksi lengkap kami!</p>
    <router-link to="/products">
      <q-btn color="primary" label="Lihat Product" />
    </router-link>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    return {
      slide: ref(1)
    }
  }
}
</script>

<style>
.home-page {
  text-align: center;
  padding: 20px;
}
</style>
