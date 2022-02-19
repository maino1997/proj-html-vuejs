<template>
  <div class="col text-center">
    <img :src="url" alt="partner" />
  </div>
</template>

<script>
export default {
  name: "PartnerCard",
  props: ["url"],
};
</script>

<style scoped lang="scss">
img {
  width: 100%;
}
</style>