<template>
  <div class="timer-block">
    <TimerNumber
      v-for="(timerCount, idx) of timerBlock"
      v-bind:key="idx"
      v-bind:timerCount="timerCount"
    />
    <hr />
    <TimerStart />
  </div>
</template>

<style lang='scss'>
p {
  padding: 0;
  text-align: center;
  font-family: 'Gotham Pro', sans-serif;
  font-weight: normal;
  color: #9e9e9e;
  font-size: 22px;
  margin: 22px 0 20px 0;
}

hr {
  height: 2px;
  border: 0;
  background-color: #9e9e9e;
  margin: 0;
}

.timer-block {
  width: 33.333%;
  background: #696969;
}
</style>

<script>
import TimerNumber from '@/components/TimerNumber.vue'
import TimerStart from '@/components/TimerStart.vue'
export default {
  props: ['timerBlock'],
  components: {
    TimerNumber,
    TimerStart
  }
}
</script>
