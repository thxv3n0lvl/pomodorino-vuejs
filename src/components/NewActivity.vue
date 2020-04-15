<template>
  <div class="activity--new">
    <input class="input"
           type="text"
           name="activity"
           placeholder="New task"
           @keyup.enter.prevent="record">
  </div>
</template>

<script>
export default {
  methods: {
    record(e) {
      this.$emit('activity', e.target.value)
    }
  }
}
</script>

<style scoped>
.activity--new  {
  grid-area: newactivity;
  display: flex;
  justify-content: center;
  margin-top: 8%;
}
.input {
  margin-top: 5%;
  width: 272px;
  height: 51px;
  background: #BFD7EA;
  color: #FEFBFB;
  padding-left: 13px;
  padding-right: 13px;
  border-radius: 12px;
  border: none;
  font-size: 18px;
}
.input:focus {
  background-color: #EBF1F5;
  color: #7C7C7C;
}
</style>
