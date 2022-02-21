<template>
  <div class="col-4">
    <div class="card-show">
      <figure>
        <img :src="url" alt="image" />
        <h4>{{ card.title }}</h4>
        <figcaption id="date">{{ card.date }}</figcaption>
      </figure>
      <hr v-if="show" />
      <p>{{ card.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "ShowCard",
  props: ["card", "url", "show"],
};
</script>

<style scoped lang="scss">
.card-show {
  background-color: white;
  font-family: Raleway, Arial, Helvetica, sans-serif;
}
img {
  width: 100%;
}
h4 {
  margin-top: 20px;
  padding: 20px;
  letter-spacing: 1px;
}
hr {
  border-color: rgb(205, 205, 205);
  height: 1px;
  width: 90%;
  margin: auto;
}
figcaption {
  padding: 0 20px;
  margin-bottom: 5px;
}
p {
  padding: 20px;
  color: rgb(116, 116, 116);
}
</style>