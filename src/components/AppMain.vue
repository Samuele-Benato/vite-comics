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
  <div class="jumbotron">
    <span>CURRENT SERIES</span>
  </div>
  <main>
    <div class="container">
      <ul>
        <li v-for="(card, index) in cards" :key="index">
          <AppCard :card="card" />
        </li>
      </ul>
      <button>LOAD MORE</button>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@use "../assets/styles/partials/mixins" as *;
.jumbotron {
  margin-top: 100px;
  height: 400px;
  position: relative;
  background-image: url("/img/jumbotron.jpg");
  background-repeat: no-repeat;
  background-size: 100%;
  span {
    position: absolute;
    bottom: -7%;
    left: 15%;
    padding: 10px 25px;
    border-radius: 5px;
    border: none;
    background-color: #2883fa;
    color: white;
    font-weight: 700;
    font-size: 1rem;
    margin: 1rem;
  }
}
main {
  background-color: #191919;
  padding-top: 2rem;
  .container {
    text-align: center;
    ul {
      @include center();
      flex-wrap: wrap;
      li {
        @include center();
        width: calc(100% / 6);
        aspect-ratio: 1;
        padding: 1rem;
      }
    }
    button {
      padding: 10px 25px;
      border-radius: 5px;
      border: none;
      background-color: #2883fa;
      color: white;
      font-weight: 700;
      font-size: 0.7rem;
      margin: 1rem;
    }
  }
}
</style>
