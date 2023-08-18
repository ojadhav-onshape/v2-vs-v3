<script lang="ts">
import Child from "./components/Child.vue"

export default {
  components : {Child},
  methods: {
    showMessage(){
      window.alert("buttonPressed")
    }
  }
}
</script>

<template>
  <Child @buttonPressed="showMessage()"/>
</template>


