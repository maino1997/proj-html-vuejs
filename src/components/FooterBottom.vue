<template>
  <div class="footer-bottom">
    <div class="container">
      <div class="content">
        <ul class="d-flex">
          <li v-for="right in rights" :key="right.text">
            <a href="#">
              {{ right.text }}
            </a>
          </li>
        </ul>
        <ul class="d-flex">
          <li v-for="link in socialLinks" :key="link.class">
            <a href="#"><i class="bi" :class="link.class"></i></a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterBottom",
  props: ["rights"],
  data() {
    return {
      socialLinks: [
        {
          class: "bi-facebook",
        },
        {
          class: "bi-twitter",
        },
        {
          class: "bi-youtube",
        },
        {
          class: "bi-instagram",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
.footer-bottom {
  background-color: black;
  color: rgb(116, 116, 116);
  height: 70px;
}

.container {
  height: 100%;
}

.content {
  justify-content: space-between;
  display: flex;
  height: 100%;
}

ul {
  height: 100%;
  font-size: 12px;
  li {
    height: 100%;
    margin-right: 5px;
  }
}
a {
  display: flex;
  align-items: center;
  color: rgb(116, 116, 116);
  height: 100%;
  i {
    font-size: 1.3rem;
  }
}
</style>
