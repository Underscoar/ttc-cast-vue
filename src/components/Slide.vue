<script setup>
import { onMounted } from 'vue'
import Drink from './Slides/Drink.vue'

const props = defineProps({
    id: Number,
    type: String,
    duration: Number,
    slideContent: Object,
});

onMounted(() => {
  setTimeout(function() {
    console.log('slide klaar')
  }, props.duration)
})
</script>


<template>
  <div class="slide-wrapper">
    <div class="timer-wrap">
      <div class="timer" :style="{'animation-duration': props.duration + 'ms'}"></div>
    </div>

    <Drink v-if="type === 'drink'" v-bind="props" />
  </div>
</template>