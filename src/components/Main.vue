<template>
  <main>
    <div class="container">
      <ul>
        <li v-for="(comic, index) in Comics" :key="index">
          <Cards :cover="comic.thumb" :title="comic.series" :cardIndex="index" />
        </li>
      </ul>
    </div>
  </main>
</template>

<script>
import Cards from '@/components/Cards.vue';
import Comics from '@/data/dc-comics.js';
export default {
  name: 'Main',
  components: {
    Cards,
  },

  data() {
    return {
      Comics,
    }
  },
}
</script>

<style lang="scss">
main {
    padding: 5rem 0;
    background: #1C1C1C;
    color: white;
    text-transform: uppercase;
    ul {
      list-style: none;
      display: flex;
      flex-wrap: wrap;
      align-content: center;
      justify-content: center;

      li {
        padding: 0 1rem;
        width: calc(100% / 6);
      }
    }
}
</style>