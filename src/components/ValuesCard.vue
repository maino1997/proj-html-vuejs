<template>
  <div class="col-3">
    <div class="value-card text-center">
      <figure :class="bg">
        <i class="fas" :class="icon"></i>
      </figure>
      <h3>{{ title }}</h3>
      <div class="grey-bar"></div>
      <p>{{ description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "ValuesCard",
  props: ["title", "description", "icon", "bg"],
};
</script>

<style scoped lang="scss">
@import "../sass/vars.scss";

i {
  font-size: 3.5rem;
  color: white;
}

figure {
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
  width: 120px;
  height: 120px;
  text-align: center;
  margin: auto;
  transition: 0.2s linear;
  &:hover {
    box-shadow: 0 1px 70px $my-yellow;
    background-color: $my-yellow;
    transform: scale(0.9);
    cursor: pointer;
  }
}

h3 {
  font-size: 1rem;
  font-weight: bold;
  margin-top: 20px;
}

p {
  font-size: 0.9rem;
  margin-bottom: 30px;
}

.bgG {
  background-color: #84cb01;
}
.bgR {
  background-color: #fea23e;
}

.bgB {
  background-color: #517ad2;
}

.bgL {
  background-color: #21a6b5;
}

.grey-bar {
  background-color: lightgrey;
  height: 2px;
  width: 50px;
  margin: auto;
  margin-top: 20px;
  margin-bottom: 20px;
}
</style>