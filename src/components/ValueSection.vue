<template>
  <section id="value-section">
    <div class="container">
      <Title title="Our Core Values" />
    </div>
    <div class="container-strict">
      <div class="row">
        <ValuesCard
          v-for="card in valuesCards"
          :key="card.title"
          :title="card.title"
          :icon="card.icon"
          :description="card.description"
          :bg="card.bg"
        />
      </div>
    </div>
    <div class="slider">
      <svg
        class="fusion-big-half-circle-candy"
        xmlns="http://www.w3.org/2000/svg"
        version="1.1"
        width="100%"
        height="100"
        viewBox="0 0 100 100"
        preserveAspectRatio="none"
        style="padding: 0"
        fill="rgba(245,245,245,1)"
        id="sup-svg"
      >
        <path d="M0 100 C40 0 60 0 100 100 Z"></path>
      </svg>
      <svg
        class="fusion-big-half-circle-candy"
        xmlns="http://www.w3.org/2000/svg"
        version="1.1"
        width="100%"
        height="100"
        viewBox="0 0 100 100"
        preserveAspectRatio="none"
        style="padding: 0"
        fill="rgba(245,245,245,1)"
        id="down-svg"
      >
        <path d="M0 100 C40 0 60 0 100 100 Z"></path>
      </svg>
    </div>
    <div class="container">
      <Title Title="Latest News" />
    </div>
    <div class="container-strict">
      <div class="row">
        <CardShow
          v-for="card in showCards"
          :key="card.url2"
          :card="card"
          :url="card.url2"
        />
      </div>
    </div>
  </section>
</template>

<script>
import Title from "./Title.vue";
import ValuesCard from "./ValuesCard.vue";
import CardShow from "./CardShow.vue";

export default {
  name: "ValueSection",
  components: {
    Title,
    ValuesCard,
    CardShow,
  },
  props: ["showCards"],
  data() {
    return {
      valuesCards: [
        {
          title: "Great Service",
          description:
            "Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia",
          icon: "fa-house",
          bg: "bgL",
        },
        {
          title: "Highest Standard",
          description:
            "Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia",
          icon: "fa-cog",
          bg: "bgB",
        },
        {
          title: "Professional Team",
          description:
            "Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia",
          icon: "fa-users",
          bg: "bgR",
        },
        {
          title: "Creative Solutions",
          description:
            "Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia",
          icon: "fa-lightbulb",
          bg: "bgG",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
#value-section {
  padding-top: 80px;
  background-color: #f5f5f5;
}

.slider {
  background-image: url("https://avada.theme-fusion.com/construction/wp-content/uploads/sites/55/2015/12/home-parallax-144609983.jpg");
  min-height: 500px;
  background-position: center;
  position: relative;
  #sup-svg {
    position: absolute;
    top: 0px;
    transform: rotate(180deg);
    // background-color: #f5f5f5;
  }
  #down-svg {
    position: absolute;
    bottom: 0px;
    // background-color: #f5f5f5;
  }
}

img {
  width: 100%;
}
</style>