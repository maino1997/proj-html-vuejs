<template>
  <div class="col-3">
    <div class="card-invisible text-center">
      <i class="bi" :class="icon"></i>
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
  font-size: 4rem;
}
p {
  color: white;
}
</style>