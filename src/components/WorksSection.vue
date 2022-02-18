<template>
  <section>
    <div class="container">
      <Title Title="Specialists In Modern Construction" />
      <div class="row">
        <GreyCard
          v-for="title in titles"
          :key="title"
          :title="title"
          :description="description"
        />
      </div>
    </div>

    <div class="statistic">
      <svg
        class="fusion-big-half-circle-candy"
        xmlns="http://www.w3.org/2000/svg"
        version="1.1"
        width="100%"
        height="100"
        viewBox="0 0 100 100"
        preserveAspectRatio="none"
        style="padding: 0"
        fill="rgba(255,255,255,1)"
        id="top-svg"
      >
        <path d="M0 100 C40 0 60 0 100 100 Z"></path>
      </svg>
      <div class="container-strict">
        <div class="row">
          <InvisibleCard
            v-for="card in invisibleCards"
            :key="card.desc"
            :desc="card.desc"
            :count="card.count"
          />
        </div>
      </div>
      <svg
        class="fusion-big-half-circle-candy"
        xmlns="http://www.w3.org/2000/svg"
        version="1.1"
        width="100%"
        height="100"
        viewBox="0 0 100 100"
        preserveAspectRatio="none"
        style="padding: 0"
        fill="rgba(255,255,255,1)"
        id="bottom-svg"
      >
        <path d="M0 100 C40 0 60 0 100 100 Z"></path>
      </svg>
    </div>

    <div class="recent-work">
      <div class="container">
        <Title Title="Explore Recent Work" />
        <div class="row">
          <CardShow v-for="card in showCards" :key="card.url1" :card="card" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Title from "./Title.vue";
import GreyCard from "./GreyCard.vue";
import InvisibleCard from "./InvisibleCard.vue";
import CardShow from "./CardShow.vue";

export default {
  name: "WorksSection",
  components: {
    Title,
    GreyCard,
    InvisibleCard,
    CardShow,
  },
  props: ["showCards"],
  data() {
    return {
      titles: ["Buildings", "Renovate", "Construct", "Exclusive"],
      description:
        "Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia",

      invisibleCards: [
        {
          desc: "PLANNING APPLICATIONS",
          count: 3534,
          icon: "<i class='fas fa-folder'></i>",
        },
        {
          desc: "COMPLETED PROJECTS",
          count: 896,
          icon: "<i class='fas fa-folder'></i>",
        },
        {
          desc: "TRAINED PROFESSIONALS",
          count: 172,
          icon: "<i class='fas fa-folder'></i>",
        },
        {
          desc: "INTERNATIONAL OFFICES",
          count: 19,
          icon: "<i class='fas fa-folder'></i>",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../sass/vars.scss";
section {
  padding: 100px 0;
}

#top-svg {
  position: absolute;
  top: 0px;
  transform: rotate(180deg);
}

#bottom-svg {
  position: absolute;
  bottom: 0px;
}

.statistic {
  min-height: 500px;
  background-image: url("https://avada.theme-fusion.com/construction/wp-content/uploads/sites/55/2015/12/home-244125289.jpg");
  position: relative;
  display: flex;
  align-items: center;
}
</style>