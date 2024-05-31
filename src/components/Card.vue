<script scoped>
import {defineComponent, ref} from "vue";

export default defineComponent({
  name: 'Card',
  props: {
    arrayCard: Array
  },
  setup() {
    return {
    }
  }
})
</script>

<template>

  <div class="cards">
    <ul v-for="card in arrayCard" :key="card.name">
      <li>
        <img :src="card.src" :alt="card.alt">
        {{ card.name }} — {{ card.age }}
      </li>
    </ul>
  </div>

</template>

<style scoped>
ul{
  list-style-type: none;
}
ul li img{
  width: 200px;
}
</style>
