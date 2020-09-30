<template>
  <div class='timer-block'>
    <div class='timer-block__plus'></div>
  </div>
</template>

<style lang='scss'>
.timer-block__plus {
  position: relative;
  top: 50%;
  right: 0;
  bottom: 0;
  left: 0;
  margin: auto;
  display: flex;
  justify-content: center;
  align-items: center;

    &::before {
      content: "";
      position: absolute;
      width: 20px;
      height: 3px;
      background-color: #9E9E9E;
      top:50%;
      margin:auto;
    }

    &::after {
      content: '';
      position: absolute;
      margin: 4px 0 0 -1px;
      width: 3px;
      height: 20px;
      background-color: #9E9E9E;
    }
}
</style>
