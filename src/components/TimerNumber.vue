<template>
    <p>{{ timerCount.text }}</p>
</template>

<script>
export default {
  props: {
    timerCount: {
      type: Object,
      required: true
    }
  }
}
</script>

<style lang='scss' >
</style>
