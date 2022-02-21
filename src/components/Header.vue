<template>
  <header>
    <div class="container">
      <div class="header-content">
        <img src="../assets/construction_mobile_logo.png" alt="logo" />
        <div class="right-block">
          <ul>
            <li v-for="link in headerLinks" :key="link.text">
              <a :href="link.link">{{ link.text }}</a>
            </li>
          </ul>
          <YellowButton ButtonText="Get Quote" />
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import YellowButton from "./YellowButton.vue";
export default {
  components: { YellowButton },
  name: "Header",
  props: ["headerLinks", "showCards"],
};
</script>

<style scoped lang="scss">
@import "../sass/vars.scss";

header {
  padding: 30px 0;
  background-color: white;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 10;
  box-shadow: 0 3px 10px rgb(0 0 0 / 0.2);
}

.header-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

ul {
  display: flex;
  height: 78px;
  li {
    display: flex;
    align-items: center;
    height: 100%;
    margin-left: 40px;
    a {
      height: 100%;
      display: flex;
      align-items: center;
      font-size: 15px;
      font-weight: 500;
      &:hover {
        color: $my-yellow;
      }
    }
  }
}

.right-block {
  display: flex;
  align-items: center;
  button {
    height: 50px;
    margin-left: 50px;
  }
}
</style>