<script>
export default {
  data() {
    return {
      title: "Content",
    };
  },
};
</script>

<template>
  <main>
    <div class="container">
      <div>{{ title }}</div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@use "../assets/styles/partials/mixins" as *;
main {
  margin-top: 100px;
  background-color: grey;
  min-height: 100px;
  .container {
    height: 100%;
    div {
      height: 100%;
      @include center("center");
    }
  }
}
</style>
