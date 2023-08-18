<script lang="ts">
import Child from "./components/Child.vue";

export default {
  components: { Child },
  methods: {
    showMessage() {
      window.alert("Works!!");
    },
  },
};
</script>

<template>
  <Child @buttonPressed="showMessage()" />
</template>
