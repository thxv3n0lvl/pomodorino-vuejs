<template>
  <div class="activty--in-progress">
    {{ inProgress }}
  </div>
</template>

<script>
export default {
  props: {
    inProgress: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
.activty--in-progress {
  grid-area: activity;
  justify-self: center;
  margin-top: 8%;
  font-size: 24px;
}
</style>
