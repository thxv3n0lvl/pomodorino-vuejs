<template>
  <div class="timer--actions">
    <div class="button button--start">START</div>
    <div class="button button--pause">PAUSE</div>
  </div>
</template>

<style scoped>
.timer--actions {
  grid-area: actions;
  display: flex;
  justify-content: space-evenly;
  margin-top: 8%;
}
.button {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: red;
  width: 100px;
  height: 43px;
  font-size: 18px;
  border-radius: 8px;
  box-shadow: 0px 1px 5px rgba(0, 0, 0, 0.25);
  font-weight: bold;
  cursor: default;
}
.button--start {
  background-color: #F2A105;
}
.button--pause {
  background-color: #3495A0;
}
</style>
