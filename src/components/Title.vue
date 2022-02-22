<template>
  <div class="row">
    <div class="col-8 d-flex flex-column text-center">
      <h3>{{ Title }}</h3>
      <div class="yellow-bar"></div>
      <p class="text-center" v-if="show">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua ut enim ad minim
        veniam.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Title",
  components: {},
  props: ["Title", "show"],
};
</script>

<style scoped lang="scss">
@import "../sass/vars.scss";
.yellow-bar {
  height: 2px;
  background-color: $my-yellow;
  width: 200px;
  margin: 30px 0;
}
.row {
  justify-content: center;
  margin-bottom: 50px;
}

.col-8 {
  padding-top: 30px;
  align-items: center;
}

p {
  line-height: 34.05px;
  color: rgb(116, 116, 116);
  font-weight: 500;
}
</style>