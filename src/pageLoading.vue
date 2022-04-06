<script setup>
import { onMounted, ref } from 'vue'

const isLoaded = ref(false)

onMounted(() => {
  document.onreadystatechange = () => {
    if (document.readyState === 'complete') {
      isLoaded.value = true
    }
  }
})

</script>

<template lang="pug">
#page-loader(v-if="!isLoaded")
  .dot
  .dot
  .dot
  .dot
</template>

<style lang="scss">
$colors: #8cc271, #68beeb, #f5aa39, #e9643b;

#page-loader {
  display: flex;
  justify-content: center;
  align-items: center;
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background-color: #333;
  z-index: 10000;
  .dot {
    width: 40px;
    height: 40px;
    margin-right: 10px !important;
    border-radius: 50%;
    @for $i from 1 through length($colors) {
      &:nth-child(#{$i}) {
        background-color: nth($colors, $i);
      }
    }

    &:first-child {
      animation: bouncing 2s infinite ease-in-out;
    }
    &:nth-child(2) {
      animation: bouncing 2s infinite ease-in-out 0.3s;
    }
    &:nth-child(3) {
      animation: bouncing 2s infinite ease-in-out 0.5s;
    }
    &:last-child {
      animation: bouncing 2s infinite ease-in-out 0.7s;
    }
  }
}

@keyframes bouncing {
  40% {
    transform: translateY(-60px);
  }
  50% {
    transform: translateY(0);
  }
}

</style>
