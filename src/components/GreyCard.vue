<template>
  <div class="col-3">
    <div class="card">
      <div class="over">
        <h4>Artfully Created</h4>
        <p>{{ description }}</p>
        <button>GET A QUOTE</button>
      </div>
      <div class="icon-container">
        <figure>
          <i class="bi" :class="icon"></i>
        </figure>
      </div>
      <h3>{{ title }}</h3>
      <p>{{ description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "GreyCard",
  props: ["title", "description", "icon"],
};
</script>

<style scoped lang="scss">
@import "../sass/vars.scss";

.card {
  background-color: #f5f5f5;
  border-radius: 10px;
  text-align: center;
  padding: 10px;
  border: 0;
  position: relative;
  transition: transform 0.3s linear;
  margin-bottom: 80px;

  &:hover .over {
    opacity: 1;
  }
  &:hover {
    transform: rotate3d(0, 1, 0, 180deg);
  }
}

.icon-container {
  display: flex;
  justify-content: center;
}

h3 {
  margin-bottom: 20px 0;
  line-height: 35px;
}

figure {
  margin-top: 15px;
  border: 2px solid grey;
  border-radius: 50%;
  height: 65px;
  width: 65px;
  display: flex;
  justify-content: center;
  align-items: center;
  color: rgb(116, 116, 116);
}

p {
  font-size: 15px;
  color: rgb(116, 116, 116);
  margin-bottom: 70px;
  margin-top: 10px;
  font-weight: 500;
  line-height: 34.05px;
}

.bi {
  font-size: 2rem;
}

.over {
  opacity: 0;
  padding-top: 40px;
  background-color: $my-yellow;
  min-height: 305px;
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  border-radius: 10px;
  transform: rotateY(180deg);
  transition: opacity 0.1s linear 0.05s;

  button {
    background-color: white;
    opacity: 0.5;
    border: 0;
    padding: 10px 15px;
  }
}
</style>