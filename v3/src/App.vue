<script lang="ts">
import CamelEmitButton from "./components/CamelEmitButton.vue";
import KebabEmitButton from "./components/KebabEmitButton.vue";
import {version} from "vue";

export default {
  data() {  
    return {version}
  },
  components: { KebabEmitButton, CamelEmitButton },
  methods: {
    showMessage() {
      window.alert("Works!!");
    },
  },
};
</script>

<template>
  <div class="container">
    <h1>Vue {{ version }} </h1>
    <KebabEmitButton @button-clicked="showMessage()">
      emit - kebab, listen - kebab
    </KebabEmitButton>

    <KebabEmitButton @buttonClicked="showMessage()">
      emit - kebab, listen - camel
    </KebabEmitButton>

    <CamelEmitButton @button-clicked="showMessage()">
      emit - camel, listen - kebab
    </CamelEmitButton>

    <CamelEmitButton @buttonClicked="showMessage()">
      emit - camel, listen - camel
    </CamelEmitButton>
  </div>
</template>

<style>
.container {
  display: flex;
  flex-flow: column;
  align-items: center;
}
</style>
