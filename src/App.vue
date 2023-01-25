<script setup>
  import Slide from './components/Slide.vue'
  import { reactive } from 'vue'

  let allSlides = [
    {
      id: 0,
      type: 'drink',
      duration: 5000,
      slideContent: {
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
        animate: {
          bottomBar: {
            animateIn: true,
            animateOut: false
          },
          breadcrumbs: {
            animateIn: true,
            animateOut: false
          },
          productMainPhotos: {
            animateIn: true,
            animateOut: true
          },
          productTitle: {
            animateIn: true,
            animateOut: true
          },
          productPrice: {
            animateIn: true,
            animateOut: true
          },
        },
      }
    },
  ]
</script>

<template>
  <Slide v-for="slide in allSlides" :key="slide.id" v-bind="slide" />
</template>
