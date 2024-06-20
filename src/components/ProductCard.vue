<template>
  <q-card class="q-mb-md" style="width: 300px;">
    <q-img :src="product.image" :alt="product.name" />
    <q-card-section>
      <div class="text-h6">{{ product.name }}</div>
      <div class="text-subtitle1">{{ product.price }}</div>
    </q-card-section>
    <q-card-actions align="right">
      <q-btn flat label="Add to Cart" color="primary" @click="addToCart(product)" />
    </q-card-actions>
  </q-card>
</template>

<script>
export default {
  props: {
    product: {
      type: Object,
      required: true
    }
  },
  methods: {
    addToCart(product) {
      this.$emit('add-to-cart', product);
    }
  }
}
</script>
