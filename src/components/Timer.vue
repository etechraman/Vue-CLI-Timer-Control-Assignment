<template>
  <div>
    <p>{{stopwatch}}</p>
  </div>
</template>

<script>
export default {
  name: "Timer",
  props: {
    stopwatch:{
      default: "00:00:00",
    }
  },
  // data() {
  //   return {
  //     elapsedTime: 0,
  //     timer: undefined,
  //   };
  // },
  // computed: {
  //   formattedElapsedTime() {
  //     const date = new Date(null);
  //   //   console.log(date);
  //   //   console.log(this.elapsedTime);
  //   //   console.log(date.setSeconds(this.elapsedTime / 1000));
  //     date.setSeconds(this.elapsedTime / 1000);
  //     const utc = date.toUTCString();
  //   //   console.log(utc);
  //   //   console.log(utc.substr(utc.indexOf(":") - 2, 8));
  //     return utc.substr(utc.indexOf(":") - 2, 8);
  //   },
  // },
};
</script>
