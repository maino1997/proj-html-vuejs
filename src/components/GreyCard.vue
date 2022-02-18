<template>
  <div class="col-3">
    <div class="card">
      <i class="fas fa-building"></i>
      <h3>{{ title }}</h3>
      <p>{{ description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "GreyCard",
  props: ["title", "description"],
};
</script>

<style scoped lang="scss">
.card {
  background-color: #f5f5f5;
  border-radius: 10px;
  text-align: center;
  padding: 10px;
  border: 0;
}

p {
  font-size: 15px;
}

.fas {
  font-size: 3rem;
  margin-bottom: 20px;
}
</style>