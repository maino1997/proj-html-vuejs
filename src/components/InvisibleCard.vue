<template>
  <div class="col-3">
    <div class="card-invisible">
      <i class="fas fa-building"></i>
      <h3>{{ count }}</h3>
      <p>{{ desc }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "InvisibleCard",
  props: ["count", "desc", "icon"],
};
</script>

<style scoped lang="scss">
@import "../sass/vars.scss";

h3,
i {
  color: $my-yellow;
}
p {
  color: white;
}
</style>