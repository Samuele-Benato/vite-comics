<script>
export default {
  data() {
    return {
      linksH: [
        {
          name: "CHARACTERS",
          url: "#",
          active: false,
        },
        {
          name: "COMICS",
          url: "#",
          active: false,
        },
        {
          name: "MOVIES",
          url: "#",
          active: false,
        },
        {
          name: "TV",
          url: "#",
          active: false,
        },
        {
          name: "GAMES",
          url: "#",
          active: false,
        },
        {
          name: "COLLECTIBLES",
          url: "#",
          active: false,
        },
        {
          name: "VIDEOS",
          url: "#",
          active: false,
        },
        {
          name: "FANS",
          url: "#",
          active: false,
        },
        {
          name: "NEWS",
          url: "#",
          active: false,
        },
        {
          name: "SHOP",
          url: "#",
          active: true,
        },
      ],
      urlLogo: "/img/dc-logo.png",
    };
  },
  methods: {
    linkActive(link) {
      link.active == true;
    },
  },
};
</script>

<template>
  <header>
    <div class="container">
      <div class="image-container">
        <img :src="urlLogo" alt="Logo" />
      </div>
      <ul>
        <li
          v-for="link in linksH"
          :class="link.active ? 'active-line' : ''"
          @click="linkActive(link)"
        >
          <a :href="link.url">{{ link.name }}</a>
        </li>
      </ul>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use "../assets/styles/partials/mixins" as *;

header {
  .container {
    @include center("between");
    .image-container {
      width: 80px;
      img {
        width: 100%;
      }
    }
    ul {
      @include center();
      .active-line {
        margin-bottom: auto;
        box-shadow: 0 7px 0 0 #2883fa;
        a {
          color: #2883fa;
        }
      }
      li {
        font-size: 0.75rem;
        font-weight: 600;
        padding: 0 0.5rem;
      }
    }
  }
  @include center("null");
  height: 100px;
  background-color: white;
  position: fixed;
  z-index: 1;

  left: 0;
  top: 0;
  right: 0;
  opacity: 95%;
}
</style>
