<template>
  <div class="timer">
      <div class="timer--countdown">{{ time }}</div>
      <div>min</div>
  </div>
</template>

<script>
export default {
  props: {
    time: {
      type: Number,
      required: true,
      default: 25
    }
  }
}
</script>

<style scoped>
.timer {
  background: rgba(196, 196, 196, 0.47);
  grid-area: timer;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.timer--countdown {
  font-size: 46px;
}
</style>
