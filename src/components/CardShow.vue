<template>
  <div class="col-4">
    <div class="card-show">
      <img :src="card.url1" alt="image" />
    </div>
  </div>
</template>

<script>
export default {
  name: "ShowCard",
  props: ["card"],
};
</script>

<style>
</style>