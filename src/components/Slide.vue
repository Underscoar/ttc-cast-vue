<script setup>
import Drink from './Slides/Drink.vue'

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
  <div v-if="type === 'drink'" class="slide-wrapper">
    <Drink v-bind="props" />
  </div>
</template>