<template>
  <div>
    <button @click="handleButtonPress">
      <h1>Click</h1>
    </button>
  </div>
</template>

<script lang="ts">
export default {
  methods: {
    handleButtonPress() {
      this.$emit("buttonPressed");
    },
  },
};
</script>

<style scoped>
div {
  margin: auto;
}
</style>
