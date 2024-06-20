<template>
  <q-page class="q-pa-md">
    <div class="contact-content">
      <div class="contact-box">
        <h2 class="heading">Kontak Kami</h2>
        <p class="description">Silakan isi formulir di bawah ini dan kami akan menghubungi Anda sesegera mungkin.</p>

        <!-- Formulir Kontak -->
        <q-form @submit="onSubmit">
          <q-input filled v-model="name" label="Nama" class="q-mb-md" prepend-icon="mdi-account" />
          <q-input filled v-model="email" label="Email" type="email" class="q-mb-md" prepend-icon="mdi-email" />
          <q-input filled v-model="subject" label="Subjek" class="q-mb-md" prepend-icon="mdi-message" />
          <q-input filled v-model="message" label="Pesan" type="textarea" autogrow class="q-mb-md" prepend-icon="mdi-comment-text" />
          <q-btn type="submit" label="Kirim" color="primary" class="submit-button" />
        </q-form>
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      email: '',
      subject: '',
      message: ''
    }
  },
  methods: {
    onSubmit() {
      // Lakukan sesuatu dengan data form, seperti mengirim ke server
      console.log('Form submitted', this.name, this.email, this.subject, this.message);
      // Reset form
      this.name = '';
      this.email = '';
      this.subject = '';
      this.message = '';
    }
  }
}
</script>

<style scoped>
.contact-content {
  margin-top: 20px;
  display: flex;
  justify-content: center;
}

.contact-box {
  width: 100%;
  max-width: 600px;
  border: 2px solid #FF4081;
  /* Garis tepi */
  border-radius: 10px;
  /* Sudut bulat */
  padding: 20px;
  /* Ruang dalam kotak */
  background-color: #FFE0F7;
}

.heading {
  font-size: 28px;
  font-weight: bold;
  color: #FF4081;
  margin-bottom: 10px;
  text-align: center;
}

.description {
  font-size: 16px;
  color: #333;
  text-align: center;
  margin-bottom: 20px;
}

.submit-button {
  width: 100%;
}

.q-input {
  border-radius: 25px;
  background-color: #FFF3E0;
  color: #333;
}

.q-input__control {
  border-radius: 25px;
  background-color: #FFF3E0;
  color: #333;
}

.q-field__label {
  color: #FF4081;
}

.q-field__control {
  margin-top: 10px;
}

.q-field__append {
  margin-top: 10px;
}

</style>
