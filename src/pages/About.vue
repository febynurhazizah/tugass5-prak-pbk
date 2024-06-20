<template>
  <div class="container">
    <div class="about">
      <h1>Tentang Kami</h1>
      <p>Selamat datang di Toko Bunga Indah!</p>
      <p>Kami adalah toko bunga online terkemuka yang menyediakan berbagai jenis bunga segar dan rangkaian bunga indah untuk berbagai kesempatan istimewa Anda.</p>
      <p>Dengan pengalaman bertahun-tahun dalam industri bunga, kami bangga menyediakan layanan yang luar biasa, kualitas bunga yang terjamin, dan pengalaman belanja online yang mudah dan menyenangkan bagi pelanggan kami.</p>
      <div class="box">
        <h2><i class="fas fa-eye"></i> Visi Kami</h2>
        <p>Visi kami adalah menjadi destinasi utama untuk pembelian bunga online, memberikan inspirasi dan kebahagiaan melalui keindahan bunga dan rangkaian bunga kami.</p>
      </div>
      <div class="box">
        <h2><i class="fas fa-bullseye"></i> Misi Kami</h2>
        <p>Misi kami adalah untuk memberikan layanan pelanggan yang luar biasa, menyediakan bunga berkualitas tinggi yang segar dan indah, serta menciptakan pengalaman belanja yang menyenangkan bagi setiap pelanggan kami.</p>
      </div>
      <div class="box">
        <h2><i class="fas fa-users"></i> Tim Kami</h2>
        <p>Kami memiliki tim yang berdedikasi dan bersemangat, yang selalu siap membantu Anda dalam memilih bunga yang sempurna untuk setiap kesempatan, mulai dari pernikahan hingga ulang tahun, ucapan selamat, dan banyak lagi.</p>
      </div>
      <div class="box">
        <h2><i class="fas fa-envelope"></i> Hubungi Kami</h2>
        <p>Jika Anda memiliki pertanyaan atau membutuhkan bantuan, jangan ragu untuk menghubungi kami melalui email atau telepon. Kami siap membantu Anda!</p>
        <p>Email: info@ivonyshop.com</p>
        <p>Telepon: 0822-3475-7899</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
  background-color: #f4f4f4;
}

.about h1 {
  font-size: 24px;
  margin-bottom: 10px;
}

.about p {
  font-size: 16px;
  line-height: 1.6;
}

.about .box {
  border: 1px solid #ccc;
  padding: 20px;
  margin-bottom: 20px;
  transition: transform 0.3s ease, background-color 0.3s ease, box-shadow 0.3s ease;
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
}

.about .box:hover {
  transform: translateY(-5px);
  background-color: #f4f4f4;
  box-shadow: 0px 8px 16px rgba(0, 0, 0, 0.2);
}

.about h2 {
  font-size: 20px;
  margin-top: 20px;
  margin-bottom: 10px;
  display: flex;
  align-items: center;
}

.about h2 i {
  margin-right: 10px;
}
</style>
