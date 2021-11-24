<template>
  <main>
    <div class="container">
      <div class="main-title">
        <h1>
          CURRENT SERIES
        </h1>
      </div>
      <ul>
        <li v-for="(comic, index) in Comics" :key="index">
          <Cards :cover="comic.thumb" :title="comic.series" :cardIndex="index" />
        </li>
      </ul>
      <div class="load-btn">
        <h3>
          LOAD MORE
        </h3>
      </div>
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

<style scoped lang="scss">
main {
    padding-bottom: 1rem;
    background: #1C1C1C;
    color: white;
    text-transform: uppercase;

    .main-title {
      transform: translateY(-50%);
      display: inline-block;
      padding: 1rem 2.5rem;
      text-align: center;
      background-color: #0282F9;
    }

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

    .load-btn {
      width: 16%;
      padding: 0.5rem;
      display: flex;
      justify-content: center;
      margin: 0 auto;
      background-color: #0282F9;
      border: 2px solid transparent;
      transition: background, border, color, 0.3s;
      &:hover {
        cursor: pointer;
        background-color: transparent;
        border: 2px solid #0282F9;
        color: #0282F9;
      }
    }
}
</style>