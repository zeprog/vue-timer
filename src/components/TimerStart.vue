<template>
  <div class="panel-block">
    <button class="play-button">
      <div
      v-on:click="AddClass"
      v-bind:class="{ stop: isRemove, play: isActive }"
      />
    </button>
    <button>
      <div class="break"></div>
    </button>
  </div>
</template>

<style lang="scss">
button {
  border: none;
  padding: 0;
  background-color: transparent;
  outline: none;
}

.panel-block {
  display: flex;
  justify-content: center;
  margin: 20px 0;
}

.play-button {
  margin-right: 48px;
}

.play {
  border: 8px solid transparent;
  border-left: 15px solid #9E9E9E;
  cursor: pointer;
}

.break {
  height: 17px;
  width: 17px;
  background: #9E9E9E;
  cursor: pointer;
}

.stop {
  height: 17px;
  width: 3px;
  background: #9E9E9E;
  cursor: pointer;
  margin-right: 20px;
  &::after {
    content: '';
    display: block;
    height: 17px;
    width: 3px;
    background: #9E9E9E;
    margin-left: 7px;
  }
}
</style>

<script>
export default {
  data () {
    return {
      isActive: true,
      isRemove: false
    }
  },
  methods: {
    AddClass: function () {
      this.isActive = !this.isActive
      this.isRemove = !this.isRemove
    }
  }
}
</script>
