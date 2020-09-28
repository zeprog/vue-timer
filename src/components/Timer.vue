<template>
  <div class='timer-block'>
    <TimerNumber
      v-for="(timerCount, idx) of timerBlock"
      v-bind:key="idx"
      v-bind:timerCount="timerCount"
    />
    <hr>
  </div>
</template>

<style lang='scss'>
    p {
        padding: 0;
        text-align: center;
        font-family: 'Gotham Pro', sans-serif;
        font-weight: normal;
        color: #9E9E9E;
        font-size: 22px;
        margin: 22px 0 20px 0;
    }

    .timer-block {
        width: 33.333%;
        height: 120px;
        background: #696969;
    }
</style>

<script>
import TimerNumber from '@/components/TimerNumber.vue'
export default {
  props: ['timerBlock'],
  components: {
    TimerNumber
  }
}
</script>
