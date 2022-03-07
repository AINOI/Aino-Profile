<script setup>
import { ref } from 'vue'
const scroll = ref(false)
window.addEventListener('scroll', () => {
  scroll.value = (window.scrollY > 0)
})

const lastCircle = document.getElementsByClassName('circle:nth-child(6)')

</script>

<template lang="pug">
#section.section1(:class="{scroll}")
  .titleBox
    .titleText This is Aino's Profile.
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
@import './scss/allStyle.scss';

</style>
