<script>
export default {
  data() {
    return {
      linksB: [
        {
          name: "DIGITAL COMICS",
          url: "/img/buy-comics-digital-comics.png",
          active: false,
        },
        {
          name: "DC MERCHANDISE",
          url: "/img/buy-comics-merchandise.png",
          active: false,
        },
        {
          name: "SUBSCRIPTIONS",
          url: "/img/buy-comics-subscriptions.png",
          active: false,
        },
        {
          name: "COMIC SHOP LOCATOR",
          url: "/img/buy-comics-shop-locator.png",
          active: false,
        },
        {
          name: "DC POWER VISA",
          url: "/img/buy-dc-power-visa.svg",
          active: false,
        },
      ],
    };
  },
};
</script>

<template>
  <section>
    <div class="container">
      <ul>
        <li
          @click=""
          :class="link.active ? '' : ''"
          v-for="link in linksB"
          :key="link.url"
        >
          <a :href="link.url">
            <img :src="link.url" alt="buy icon" />
            <span>{{ link.name }}</span>
          </a>
        </li>
      </ul>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use "../assets/styles/partials/mixins" as *;

section {
  @include center("null");
  height: 100px;
  background-color: #2883fa;

  .container {
    @include center("around");

    ul {
      width: 100%;
      @include center("around");

      li {
        a {
          padding: 0.5rem;
          @include center();
          img {
            width: 40px;
            aspect-ratio: 1;
          }
          span {
            font-size: 0.75rem;
            color: white;
            font-weight: 600;
            padding-left: 0.25rem;
          }
        }
      }
    }
  }
}
</style>
