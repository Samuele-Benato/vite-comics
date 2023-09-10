<script>
export default {
  data() {
    return {
      links: [
        {
          title: "DC COMICS",
          subLink: [
            "Characters",
            "Comics",
            "Movies",
            "TV",
            "Games",
            "Videos",
            "News",
          ],
        },
        {
          title: "DC",
          subLink: [
            "Terms Of Use",
            "Privacy policy (New)",
            "Ad Choices",
            "Advertising",
            "Jobs",
            "Subscriptions",
            "Talent Workshops",
            "CPSC Certificates",
            "Ratings",
            "Shop Help",
            "Contact Us",
          ],
        },
        {
          title: "SITES",
          subLink: [
            "DC",
            "MAD Magazine",
            "DC Kids",
            "DC Universe",
            "DC Power Visa",
          ],
        },
        {
          title: "SHOP",
          subLink: ["Shop DC", "Shop DC Collectibles"],
        },
      ],
    };
  },
};
</script>

<template>
  <footer>
    <div class="container">
      <div class="col60">
        <ul v-for="link in links">
          <li>
            {{ link.title }}
            <a v-for="link in link.subLink" href="#">{{ link }}</a>
          </li>
        </ul>
      </div>
      <div class="col40">
        <img src="public/img/dc-logo-bg.png" alt="" />
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use "../assets/styles/partials/mixins" as *;
footer {
  max-height: 300px;
  background-image: url("/img/footer-bg.jpg");
  .container {
    @include center("between");
    .col60 {
      width: 60%;
    }
    .col40 {
      width: 40%;
      overflow: hidden;
      height: 300px;
      img {
        width: 100%;
        position: relative;
        bottom: 15%;
      }
    }
  }
}
</style>
