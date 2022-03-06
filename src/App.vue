<script setup>
import { ref } from 'vue'
const scroll = ref(false)
window.addEventListener('scroll', () => {
  scroll.value = (window.scrollY > 0)
} )

</script>

<template lang="pug">
#section.section1(:class="{scroll}")
  img.minebg(src="./assets/room.png")
  .circleGroup
    .circle
    .circle
    .circle
    .circle
    .circle
    .circle
#section.section2
  
</template>

<style lang="scss">
@import './scss/style.scss';

.scroll .kvList {
  width: 1000px;
  height: 300px;
}
</style>