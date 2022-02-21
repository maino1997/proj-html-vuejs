<template>
  <div id="app">
    <Header :headerLinks="headerLinks" />
    <Main />
    <Footer :footerContacts="footerContacts" :rights="rights" />
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

      footerContacts: [
        {
          icon: "bi-globe2",
          text: "Corporate Location 1600 Amphitheatre Parkway London WC1 1BA",
        },
        {
          icon: "bi-house",
          text: "Residential Location 9521 Broadsberry Avenue Paddington RC7 9ZA",
        },
        {
          icon: "bi-telephone",
          text: "1.800.458.556 / 1.800.532.2112",
        },
        {
          icon: "bi-telephone",
          text: "Monday – Friday: 9:00 AM – 6:00 PM",
        },
        {
          icon: "bi-clock",
          text: "Saturday – Sunday: 9:00 AM – 12:00 PM",
        },
      ],
      rights: [
        {
          text: "©COPYRIGHT 2012 - 2022 |",
        },
        {
          text: "AVADA THEME BY THEMEFUSION |",
        },
        {
          text: " ALL RIGHTS RESERVED |",
        },
        {
          text: " POWERED BY WORDPRESS",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "./sass/style.scss";
</style>
