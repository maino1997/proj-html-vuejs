<template>
  <button>{{ ButtonText }}</button>
</template>

<script>
export default {
  name: "BlackButton",
  props: ["ButtonText"],
};
</script>

<style scoped lang='scss'>
@import "../sass/vars.scss";

button {
  background-color: $my-black;
  border: 0;
  padding: 10px 32px;
  color: white;
  font-weight: 600;
  letter-spacing: 2px;

  &:hover {
    background-color: $my-yellow;
    color: black;
  }
}
</style>