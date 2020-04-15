<template>
  <div class="progress--bar">
    <span class="progress--indicator"
          :style="{width: '100%'}"></span>
  </div>
</template>

<script>
export default {
  props: {
    current: {
      type: Number,
      required: true
    },
    initialTimer: {
      type: Number,
      required: true
    }
  }
}
</script>
<style scoped>
.progress--bar {
  grid-area: progress;
  position: relative;
  background-color: #BFD7EA;
  width: 272px;
  height: 15px;
  margin-top: 16px;
  justify-self: center;
  border-radius: 5px;
}
.progress--indicator {
  position: absolute;
  width: 0;
  border-radius: inherit;
  height: inherit;
  background-color: #F2A105;
}
</style>
