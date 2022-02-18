<template>
  <div id="app">
    <Header :headerLinks="headerLinks" />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
  },
  data() {
    return {
      headerLinks: [
        {
          text: "HOME",
          link: "#",
        },
        {
          text: "ABOUT",
          link: "#",
        },
        {
          text: "SERVICIES",
          link: "#",
        },
        {
          text: "WORK",
          link: "#",
        },
        {
          text: "ARTICLES",
          link: "#",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "./sass/style.scss";
</style>
