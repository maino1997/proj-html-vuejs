<template>
  <div class="all-articles">
    <div class="grey-bar"></div>
    <a href="#">View All Project</a>
    <div class="grey-bar"></div>
  </div>
</template>

<script>
export default {
  name: "AllArticles",
};
</script>

<style lang="scss" scoped>
.all-articles {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 50px;
}

.grey-bar {
  background-color: rgb(226, 218, 218);
  height: 2px;
  width: 300px;
  margin: 0 20px;
}
a {
  color: black;
  font-size: bold;
  &:hover {
    color: black;
  }
}
</style>