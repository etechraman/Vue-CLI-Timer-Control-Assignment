<template>
  <div>
    <p>{{ stopwatch }}</p>
  </div>
</template>

<script>
export default {
  name: "Timer",
  props: {
    stopwatch: {
      default: "00:00:00",
    },
  },
};
</script>
