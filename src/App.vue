<script setup>
  import Slide from './components/Slide.vue'

  let allSlides = [
    {
      id: 0,
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
    },
    {
      id: 1,
      type: 'drink',
      breadcrumbs: {
        title: 'Menukaart TTC',
        subtitle: 'Dranken > alcoholische dranken'
      },
      name: 'Hertog Jan',
      subtitle: '300ml',
      price: '€ 2,00',
      bonnen: '2 bonnen',
      img1: 'Hertog-Jan-Fles-30cl.png',
      img2: 'Hertog-Jan-Fles-30cl.png',
    }
  ]
</script>

<template>
  <Slide v-for="slide in allSlides" :key="slide.id" v-bind="slide" />
</template>
