<template>
  <div class="home">
    <Timer />
  </div>
</template>

<script>
// @ is an alias to /src
import Timer from '@/components/Timer.vue'

export default {
  name: 'Home',
  components: {
    Timer
  }
}
</script>

<style lang='scss'>
.home {
    background: #353638;
    height: 100vh;
}
</style>
