<template>
  <div>
    <ul>
      <li v-for="button in buttons" :key="button.id">
        <button @click="$emit(button.name)">{{ button.name }}</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "control",
  data() {
    return {
      buttons: [
        { id: 1, name: "Start" },
        { id: 2, name: "Pause" },
        { id: 3, name: "Reset" },
      ],
    };
  },
};
</script>
<style>
li {
  display: inline;
}
</style>
