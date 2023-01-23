<script setup>
const props = defineProps({
    type: String,
    breadcrumbs: {
        title: String,
        subtitle: String
    },
    name: String,
    subtitle: String,
    price: String,
    bonnen: String,
    img1: String,
    img2: String,
});
</script>


<template>
    <div class="slide-main-content">
      <div class="product-main-photos">
        <div class="secondary-photo">
          <img :src="`../src/assets/products/${img1}`" width="175" alt="" />
        </div>
        <div class="main-photo">
          <img :src="`../src/assets/products/${img2}`" width="225" alt="">
        </div>
      </div>
      
      <div class="product-text-content">
        <div class="breadcrumbs">
          <h3>{{ breadcrumbs.title }}</h3>
          <h4>{{ breadcrumbs.subtitle }}</h4>
        </div>

        <div class="product-title">
          <h2>{{ name }}</h2>
          <p role="doc-subtitle">{{ subtitle }}</p>
        </div>

        <div class="product-price">
          <h2>{{ price }}</h2>
          <h3 class="bonnen">({{ bonnen }})</h3>
        </div>
      </div>
    </div>


    <div class="bottom-bar">
      <img src="../../assets/ttc-logo-wit.svg" alt="TTC logo - wit" width="300">
    </div>
</template>