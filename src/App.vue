<script setup>
  import Slide from './components/Slide.vue'

  let despoSlide = {
    type: 'drink',
    breadcrumbs: {
      title: 'Menukaart TTC',
      subtitle: 'Dranken > alcoholische dranken'
    },
    name: 'Desperados',
    subtitle: '330ml',
    price: '€ 3,00',
    bonnen: '3 bonnen',
    img1: 'desperados.33_1_2.png',
    img2: 'desperados.33_1_2.png',
  }
</script>

<template>
  <Slide v-bind="despoSlide" />
</template>
