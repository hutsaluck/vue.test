<template>
  <h2>Hello, {{name}}</h2>
</template>


<script>
import {defineComponent} from "vue";

export default defineComponent({
  name: 'App',
  components: {

  },
  setup(){
    const name = 'Yuriy'
    return {
      name
    }
  }
})
</script>
<style>

</style>
