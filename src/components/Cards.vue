<script>
import {defineComponent, ref} from "vue";

export default defineComponent({
  name: 'Cards',
  setup() {
    const arrayCard = [
      {name: "user3", age: 12, src: 'https://picsum.photos/200/300?random=1', alt: 'kitten'},
      {name: "user2", age: 12, src: 'https://picsum.photos/200/300?random=2', alt: 'kitten'},
      {name: "user4", age: 12, src: 'https://picsum.photos/200/300?random=3', alt: 'kitten'},
      {name: "user5", age: 12, src: 'https://picsum.photos/200/300?random=4', alt: 'kitten'},
      {name: "user1", age: 12, src: 'https://picsum.photos/200/300?random=5', alt: 'kitten'},
      {name: "user6", age: 12, src: 'https://picsum.photos/200/300?random=6', alt: 'kitten'},
      {name: "user7", age: 12, src: 'https://picsum.photos/200/300?random=7', alt: 'kitten'},
      {name: "user8 ", age: 12,src: 'https://picsum.photos/200/300?random=8', alt: 'kitten'},
    ]

    return {
      arrayCard
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

<style>
ul{
  list-style-type: none;
}
ul li img{
  width: 200px;
}
</style>
