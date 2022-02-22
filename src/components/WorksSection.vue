<template>
  <section>
    <div class="container">
      <Title Title="Specialists In Modern Construction" :show="true" />
      <div class="row">
        <GreyCard
          v-for="card in greyCards"
          :key="card.title"
          :title="card.title"
          :description="card.description"
          :icon="card.icon"
          :hoverTitle="card.hoverTitle"
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
            :icon="card.icon"
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
        <Title Title="Explore Recent Work" :show="true" />
        <div class="row">
          <CardShow
            v-for="card in showCards"
            :key="card.url1"
            card=""
            :url="card.url1"
            :hoverTitle="card.hoverTitle"
            :hoverTextUp="card.hoverTextUp"
            :visible1="true"
            :visible2="false"
            :visible3="false"
          />
        </div>
      </div>
    </div>
    <AllArticles />
  </section>
</template>

<script>
import Title from "./Title.vue";
import GreyCard from "./GreyCard.vue";
import InvisibleCard from "./InvisibleCard.vue";
import CardShow from "./CardShow.vue";
import AllArticles from "./AllArticles.vue";

export default {
  name: "WorksSection",
  components: {
    Title,
    GreyCard,
    InvisibleCard,
    CardShow,
    AllArticles,
  },
  props: ["showCards"],
  data() {
    return {
      greyCards: [
        {
          title: "Buildings",
          hoverTitle: "Artfully Created",
          icon: "bi-building",
          description:
            "Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia",
        },
        {
          title: "Renovate",
          hoverTitle: "Freshly New",
          icon: "bi-arrow-repeat",
          description:
            "Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia",
        },
        {
          title: "Construct",
          hoverTitle: "Perfect Lines",
          icon: "bi-house-door-fill",
          description:
            "Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia",
        },
        {
          title: "Exclusive",
          hoverTitle: "Planning",
          icon: "bi-truck",
          description:
            "Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia",
        },
      ],

      invisibleCards: [
        {
          desc: "PLANNING APPLICATIONS",
          count: 3534,
          icon: "bi-folder",
        },
        {
          desc: "COMPLETED PROJECTS",
          count: 896,
          icon: "bi-building",
        },
        {
          desc: "TRAINED PROFESSIONALS",
          count: 172,
          icon: "bi-people-fill",
        },
        {
          desc: "INTERNATIONAL OFFICES",
          count: 19,
          icon: "bi-globe2",
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
  padding: 150px 0;
}
</style>