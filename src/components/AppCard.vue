<script>
export default {
  props: {
    card: Object,
  },
};
</script>

<template>
  <figure class="card">
    <div class="image-container">
      <img :src="card.thumb" alt="film mignature" />
    </div>
    <figcaption>{{ card.series }}</figcaption>
    <figcaption>{{ card.type }}</figcaption>
    <figcaption>Price : {{ card.price }}</figcaption>
  </figure>
</template>

<style lang="scss" scoped>
@use "../assets/styles/partials/mixins" as *;
.card {
  &:hover {
    scale: 1.2;
  }
  .image-container {
    width: 100%;
    img {
      width: 100%;
    }
  }
  figcaption {
    color: white;
    text-align: left;
    font-size: 0.75rem;
    font-weight: 600;
  }
}
</style>
