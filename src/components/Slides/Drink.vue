<script setup>
import { onMounted } from 'vue'

const props = defineProps({
    type: String,
    duration: Number,
    slideContent: Object,
});

onMounted(() => {
  let allAnimations = document.querySelectorAll('.animate-in');
  allAnimations.forEach((element, index, array) => {
    setTimeout(function() {
      element.classList.remove('animate-in');
    }, (125 * index) + 100);
  });
});

</script>


<template>
    <div class="slide-main-content">

      <div class="product-main-photos to-animate">
        <div class="secondary-photo">
          <img :src="`../src/assets/products/${slideContent.img1}`" width="175" alt="" />
        </div>
        <div class="main-photo">
          <img :src="`../src/assets/products/${slideContent.img2}`" width="225" alt="">
        </div>
      </div>
      
      <div class="product-text-content">
        <div :class="`breadcrumbs to-animate ${slideContent.animate.breadcrumbs.animateIn ? 'animate-in' : ''} ${slideContent.animate.breadcrumbs.animateOut ? 'animate-out' : ''}`">
          <h3>{{ slideContent.breadcrumbs.title }}</h3>
          <h4>{{ slideContent.breadcrumbs.subtitle }}</h4>
        </div>

        <div :class="`product-title to-animate ${slideContent.animate.productTitle.animateIn ? 'animate-in' : ''} ${slideContent.animate.productTitle.animateOut ? 'animate-out' : ''}`">
          <h2>{{ slideContent.name }}</h2>
          <p role="doc-subtitle">{{ slideContent.subtitle }}</p>
        </div>

        <div :class="`product-price to-animate ${slideContent.animate.productPrice.animateIn ? 'animate-in' : ''} ${slideContent.animate.productPrice.animateOut ? 'animate-out' : ''}`">
          <h2>{{ slideContent.price }}</h2>
          <h3 class="bonnen">({{ slideContent.bonnen }})</h3>
        </div>
      </div>
    </div>


    <div :class="`bottom-bar to-animate ${slideContent.animate.bottomBar.animateIn ? 'animate-in' : ''} ${slideContent.animate.bottomBar.animateOut ? 'animate-out' : ''}`">
      <img src="../../assets/ttc-logo-wit.svg" alt="TTC logo - wit" width="300">
    </div>
</template>