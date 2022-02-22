<template>
  <div class="col-4">
    <div class="card-show">
      <figure class="figcont">
        <div class="show-over">
          <div class="show-inner">
            <figure><i class="bi bi-link-45deg"></i></figure>
            <figure><i class="bi bi-search"></i></figure>
          </div>
          <div class="show-inner-description text-white text-center">
            <h4 v-if="visible1">
              {{ hoverTitle }}
            </h4>
            <h4 v-if="visible2">
              {{ card.title }}
            </h4>
            <p v-if="visible1">{{ hoverTextUp }}</p>
            <p v-if="visible2">{{ hoverTextDown }}</p>
          </div>
        </div>
        <img :src="url" alt="image" />
      </figure>
      <h4 v-if="show">{{ card.title }}</h4>
      <figcaption v-if="show" class="date">{{ card.date }}</figcaption>
      <hr v-if="show" />
      <p v-if="show">{{ card.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "ShowCard",
  props: [
    "card",
    "url",
    "show",
    "hoverTitle",
    "hoverTextUp",
    "hoverTextDown",
    "visible1",
    "visible2",
    "visible3",
  ],
  data() {
    return {
      name: "ShowCard",
    };
  },
};
</script>

<style scoped lang="scss">
@import "../sass/vars.scss";

.card-show {
  background-color: white;
  font-family: Raleway, Arial, Helvetica, sans-serif;
  padding-bottom: 30px;
  .figcont {
    position: relative;
    &:hover .show-over {
      opacity: 1;
    }
  }
}
img {
  width: 100%;
  height: 100%;
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
.date {
  padding: 0 20px;
  margin-bottom: 10px;
  font-size: 12px;
  font-weight: 500;
}
p {
  padding: 20px;
  color: rgb(116, 116, 116);
  margin-bottom: 30px;
  font-weight: 500;
  line-height: 34.05px;
}

.show-over {
  transition: 0.2s linear;
  opacity: 0;
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  right: 0;
  background-color: $my-yellow;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  padding: 40px 0;
  .show-inner {
    display: flex;
    justify-content: center;
    align-items: center;

    figure {
      background-color: white;
      border-radius: 50%;
      height: 50px;
      width: 50px;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 0;
      margin-top: 62px;
      margin-right: 10px;
      margin-left: 10px;
      i {
        font-size: 1.6rem;
        color: black;
      }
    }
  }
}
.show-inner-description p {
  color: white;
}
.show-inner-description h4 {
  margin: 0;
  padding: 0;
}

.show-inner figure {
  margin-top: 65px;
}
</style>