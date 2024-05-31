<template>
  <h2>Hello, {{ name }}</h2>

  <div class="container">
    <button @click="flag = !flag">Click!</button>
    <h2 v-if="flag">Hello</h2>
    <h2 v-else>Bye bye</h2>
  </div>

  <div class="container">
    <button @click="count = count + 1">Click + 1</button>
    <p>{{ count }}</p>
  </div>

  <div class="container">
    <input type="text" v-model="text">
    <p>{{ text }}</p>
  </div>

  <Cards />
</template>


<script>
import {defineComponent, ref} from "vue";
import Cards from "@/components/Cards.vue";

export default defineComponent({
  name: 'App',
  components: {Cards},
  setup() {
    const name = 'Yuriy'
    const flag = ref(true)
    const count = ref(0)
    const text = ref('')
    return {
      name,
      flag,
      count,
      text
    }
  }
})
</script>
<style>

</style>
