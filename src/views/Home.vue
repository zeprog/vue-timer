<template>
  <div class="home">
    <div class="timer__wrap">
      <Timer
        v-bind:timerBlock="timerBlock"
      />
      <TimerAdd />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Timer from '@/components/Timer.vue'
import TimerAdd from '@/components/TimerAdd.vue'

export default {
  name: 'Home',
  data () {
    return {
      timerBlock: [
        { start: 0, text: '0', countStart: false }
      ]
    }
  },
  components: {
    Timer,
    TimerAdd
  }
}
</script>

<style lang='scss'>
.home {
    background: #353638;
    height: 100vh;
}

.timer__wrap {
    width: 775px;
    margin: 0 auto;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    padding-top: 72px;
}
</style>
