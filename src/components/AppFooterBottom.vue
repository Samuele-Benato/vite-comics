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
        <a>SIGN-UP NOW!</a>
      </div>
      <ul>
        <li><span>FOLLOW US</span></li>
        <li
          @click=""
          :class="link.active ? '' : ''"
          v-for="link in linksF"
          :key="link.url"
        >
          <a :href="link.url">
            <img :src="link.url" alt="social network icon" />
          </a>
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
      li {
        span {
          color: #2883fa;
          padding-right: 0.5rem;
        }
      }
      li {
        a {
          padding: 0.5rem;
        }
      }
    }
  }
}
</style>
