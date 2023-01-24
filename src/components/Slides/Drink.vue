<script setup>
import { onMounted } from 'vue'

const props = defineProps({
    type: String,
    duration: Number,
    slideContent: Object,
});

onMounted(() => {
  console.log(props.slideContent);
})
</script>


<template>
    <div class="slide-main-content">

      <div class="product-main-photos">
        <div class="secondary-photo">
          <img :src="`../src/assets/products/${slideContent.img1}`" width="175" alt="" />
        </div>
        <div class="main-photo">
          <img :src="`../src/assets/products/${slideContent.img2}`" width="225" alt="">
        </div>
      </div>
      
      <div class="product-text-content">
        <div class="breadcrumbs">
          <h3>{{ slideContent.breadcrumbs.title }}</h3>
          <h4>{{ slideContent.breadcrumbs.subtitle }}</h4>
        </div>

        <div class="product-title">
          <h2>{{ slideContent.name }}</h2>
          <p role="doc-subtitle">{{ slideContent.subtitle }}</p>
        </div>

        <div class="product-price">
          <h2>{{ slideContent.price }}</h2>
          <h3 class="bonnen">({{ slideContent.bonnen }})</h3>
        </div>
      </div>
    </div>


    <div class="bottom-bar">
      <img src="../../assets/ttc-logo-wit.svg" alt="TTC logo - wit" width="300">
    </div>
</template>