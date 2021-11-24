<template>
  <div>
      <div class="card" :class="`card-${cardIndex}`">
          <img :src="cover" :alt="title">
      </div>
      <h2>{{ title }}</h2>
  </div>
</template>

<script>
export default {
    name: 'Cards',
    props: {
        cover: String,
        title: String,
        cardIndex: Number,
    },
}
</script>

<style lang="scss">
.card {
    max-height: 190px;
    overflow: hidden;
    img {
        display: block;
        width: 100%;
    }
}

h2 {
    padding: 1.5rem 0;
}
</style>