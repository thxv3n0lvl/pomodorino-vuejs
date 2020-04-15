<template>
  <div id="app">
      <nav-bar></nav-bar>
      <timer :time="initialTimer">
      </timer>
      <progress-bar :initialTimer="initialTimer"
                    :current="currentTime"></progress-bar>
      <activity :inProgress="inProgress"></activity>
      <new-activity @activity="registerActivity"></new-activity>
      <timer-actions></timer-actions>
  </div>
</template>

<script>
import NavBar from '@/components/NavBar.vue'
import Timer from '@/components/Timer.vue'
import ProgressBar from '@/components/ProgressBar.vue'
import Activity from '@/components/Activity.vue'
import NewActivity from '@/components/NewActivity.vue'
import TimerActions from '@/components/TimerActions.vue'
export default {
  name: "App",
  components: {
    NavBar,
    Timer,
    ProgressBar,
    Activity,
    NewActivity,
    TimerActions
  },
  data() {
    return {
      inProgress: 'Add a task !',
      initialTimer: 25,
      interval: 0,
      currentTime: 0
    }
  },
  methods: {
    registerActivity(task) {
      this.inProgress = task
      this.startTimer()
    },
    startTimer() {
      this.interval = setInterval(this.countdown.bind(this),100)
    },
    countdown() {
      if(this.initialTimer == 0) {
        clearInterval(this.interval)
        return
      }
      this.currentTime = this.initialTimer -= 1
    }
  }
};
</script>

<style>
  html {
    box-sizing: border-box;
  }
  *,
  *:before,
  *:after {
    box-sizing: inherit;
  }
  body {
    background-color: #06324D;
    font-family: 'Roboto', sans-serif;
    color: #FFFCFC;
  }
  #app {
    display: grid;
    width: 100%;
    grid-template-rows: 103px 94px .5fr .8fr 1fr 1fr;
    grid-template-areas:
       "navigation"
       "timer"
       "progress"
       "activity"
       "newactivity"
       "actions"
  }
</style>
