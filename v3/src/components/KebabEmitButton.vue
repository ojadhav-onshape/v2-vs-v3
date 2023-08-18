<template>
  <button @click="$emit('button-clicked')">
    <slot></slot>
  </button>
</template>

<style scoped>
button {
  padding: 16px;
  font-size: 20px;
  background-color: dodgerblue;
  color: white;
  border-radius: 10px;
}
</style>
