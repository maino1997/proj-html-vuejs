<template>
  <button>{{ ButtonText }}</button>
</template>

<script>
export default {
  name: "YellowButton",
  props: ["ButtonText"],
};
</script>

<style scoped lang='scss'>
@import "../sass/vars.scss";

button {
  background-color: $my-yellow;
  border: 0;
  padding: 10px 25px;
}
</style>