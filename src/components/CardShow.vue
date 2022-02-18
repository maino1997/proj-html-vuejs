<template>
  <div class="col-4">
    <div class="card-show">
      <img :src="url" alt="image" />
    </div>
  </div>
</template>

<script>
export default {
  name: "ShowCard",
  props: ["card", "url"],
};
</script>

<style scoped lang="scss">
img {
  width: 100%;
}
</style>