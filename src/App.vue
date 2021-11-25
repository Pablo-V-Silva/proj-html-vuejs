<template>
  <div id="app">
    <SiteHeader :links="linksArray" />
    <SiteMain />
    <SiteFooter />
  </div>
</template>

<script>
import SiteHeader from "./components/SiteHeader.vue";
import SiteMain from "./components/SiteMain.vue";
import SiteFooter from "./components/SiteFooter.vue";

export default {
  data() {
    return {
      linksArray: [
        { link: "home" },
        { link: "about" },
        { link: "prices" },
        { link: "courses", btn: true },
        { link: "location" },
        { link: "blog" },
      ],
    };
  },
  components: {
    SiteHeader,
    SiteMain,
    SiteFooter,
  },
};
</script>

<style lang="scss">
@import "../node_modules/bootstrap/scss/bootstrap.scss";
@import url("https://fonts.googleapis.com/css2?family=Kalam:wght@700&family=Outfit:wght@100;200;300;500;600&display=swap");

#app {
  font-family: "Kalam", cursive;
  font-family: "Outfit", sans-serif;
}
</style>
