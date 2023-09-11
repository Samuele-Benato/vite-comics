<script>
export default {
  props: {
    cards: Array,
  },
};
</script>

<template>
  <figure v-for="(card, index) in cards" :key="index" class="card">
    <div class="image-container">
      <img :src="card.thumb" alt="film mignature" />
    </div>
    <figcaption>{{ card.series }}</figcaption>
    <figcaption>{{ card.type }} {{ card.price }}</figcaption>
  </figure>
</template>

<style lang="scss" scoped>
@use "../assets/styles/partials/mixins" as *;
.card {
  width: calc(100% / 6);
}
</style>
