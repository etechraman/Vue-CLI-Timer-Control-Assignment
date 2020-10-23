<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <Timer :stopwatch="formattedElapsedTime" />
    <Control @Start="start" @Pause="pause" @Reset="reset" />
  </div>
</template>

<script>
import Timer from "./components/Timer.vue";
import Control from "./components/Control.vue";

export default {
  name: "App",
  components: {
    Timer,
    Control,
  },
  data() {
    return {
      elapsedTime: 0,
      timer: null,
      stopwatch: "00:00:00",
    };
  },
  computed: {
    formattedElapsedTime() {
      const date = new Date(null);
      date.setSeconds(this.elapsedTime / 1000);
      const utc = date.toUTCString();
      return utc.substr(utc.indexOf(":") - 2, 8);
    },
  },
  methods: {
    start() {
      this.timer = setInterval(() => {
        this.elapsedTime += 1000;
      }, 1000);
    },
    pause() {
      clearInterval(this.timer);
    },
    reset() {
      this.elapsedTime = 0;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
