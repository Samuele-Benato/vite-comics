<script>
import AppCard from "./AppCard.vue";
export default {
  data() {
    return {};
  },
  props: {
    cards: Array,
  },
  components: {
    AppCard,
  },
};
</script>

<template>
  <div class="jumbotron"></div>
  <main>
    <div class="container">
      <ul>
        <li><AppCard :cards="dcCards" /></li>
      </ul>
      <button>LOAD MORE</button>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@use "../assets/styles/partials/mixins" as *;
.jumbotron {
  height: 300px;
}
main {
  background-color: #191919;
  .container {
    text-align: center;
    button {
      padding: 10px 25px;
      border-radius: 5px;
      border: none;
      background-color: #2883fa;
      color: white;
      font-weight: 700;
      font-size: 0.5rem;
      margin: 1rem;
    }
  }
}
</style>
