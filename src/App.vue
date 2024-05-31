<template>
  <h2>Hello, {{ name }}</h2>
  <br><br><br>
  <button @click="flag = !flag">Click!</button>
  <br>
  <h2 v-if="flag">Hello</h2>
  <h2 v-else>Bye bye</h2>
</template>


<script>
import {defineComponent, ref} from "vue";

export default defineComponent({
  name: 'App',
  components: {},
  setup() {
    const name = 'Yuriy'
    const flag = ref(true)
    return {
      name,
      flag
    }
  }
})
</script>
<style>

</style>
