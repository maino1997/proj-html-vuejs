<template>
  <div class="container">
    <header>
      <img src="../assets/construction_logo.png" alt="logo" />
      <ul>
        <li><a href="#">HOME</a></li>
        <li><a href="#">ABOUT</a></li>
        <li><a href="#">SERVICIES</a></li>
        <li><a href="#">WORK</a></li>
        <li><a href="#">ARTICLES</a></li>
      </ul>
      <YellowButton ButtonText="Get Quote" />
    </header>
  </div>
</template>

<script>
import YellowButton from "./YellowButton.vue";
export default {
  components: { YellowButton },
  name: "Header",
};
</script>

<style scoped lang="scss">
@import "../sass/vars.scss";

header {
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
      &:hover {
        color: $my-yellow;
        border-bottom: 4px solid $my-yellow;
      }
    }
  }
}
</style>