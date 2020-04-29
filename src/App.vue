<template>
  <div>
    <img src="./logo.png">
    <button @click="inc">Clicked {{ count }} times.</button>
    <h1>Hello Vue 3!</h1>
  </div>
</template>

<script lang="ts">
import { ref, defineComponent } from 'vue'

export default defineComponent({
  setup() {
    const count = ref(0)
    const inc = () => {
      count.value++
    }

    return {
      count,
      inc
    }
  }
})
</script>

<style scoped>
img {
  width: 200px;
}
h1 {
  font-family: Arial, Helvetica, sans-serif;
}
</style>