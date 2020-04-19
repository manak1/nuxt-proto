<template>
  <div>
    <div class="bg"></div>
    <l-header />
    <nuxt />
  </div>
</template>
<script>
import LHeader from '@/components/layout/LHeader'
export default {
  components: {
    LHeader
  }
}
</script>

<style>
.bg {
  position: absolute;
  background-color: red;
  height: 100vh;
  width: 100%;
  animation-name: inPage;
  animation-duration: 1s;
  animation-delay: 0.2s;
  animation-play-state: cubic-bezier(0.25, 0, 0, 0.24);
  animation-iteration-count: 1;
  top: -100vh;
  z-index: 2000;
}

@keyframes inPage {
  0% {
    top: 100vh;
  }

  100% {
    top: -100vh;
    display: none;
  }
}
</style>
