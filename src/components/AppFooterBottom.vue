<script>
export default {
  data() {
    return {
      linksF: [
        {
          name: "facebook",
          url: "/img/footer-facebook.png",
          active: false,
        },
        {
          name: "twitter",
          url: "/img/footer-twitter.png",
          active: false,
        },
        {
          name: "youTube",
          url: "/img/footer-youtube.png",
          active: false,
        },
        {
          name: "pinterest",
          url: "/img/footer-pinterest.png",
          active: false,
        },
        {
          name: "google maps",
          url: "/img/footer-periscope.png",
          active: false,
        },
      ],
    };
  },
};
</script>

<template>
  <footer>
    <div class="container">
      <div class="footer-button">
        <span>SIGN-UP NOW!</span>
      </div>
      <ul>
        <li><span>FOLLOW US</span></li>
        <li @click="" :class="link.active ? '' : ''" v-for="link in linksF">
          <a :href="link.url"></a>
        </li>
      </ul>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use "../assets/styles/partials/mixins" as *;

footer {
  @include center("null");
  height: 100px;
  background-color: #2a2a2a;

  .container {
    @include center("between");
    .footer-button {
      border: 2px solid #2883fa;
      padding: 0.7rem;
      color: white;
    }
    ul {
      @include center();
      span {
        color: #2883fa;
      }
    }
  }
}
</style>
