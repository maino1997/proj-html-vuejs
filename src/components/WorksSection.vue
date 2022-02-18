<template>
  <section>
    <div class="container">
      <Title Title="Specialists In Modern Construction" />
      <div class="row">
        <GreyCard
          v-for="card in greyCardS"
          :key="card.title"
          :title="card.title"
          :description="card.description"
          :icon="card.icon"
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
        <Title Title="Explore Recent Work" />
        <div class="row">
          <CardShow
            v-for="card in showCards"
            :key="card.url1"
            :card="card"
            :url="card.url1"
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
      greyCardS: [
        {
          title: "Buildings",
          icon: "fa-building",
          description:
            "Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia",
        },
        {
          title: "Renovate",
          icon: "fa-sync-alt",
          description:
            "Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia",
        },
        {
          title: "Construct",
          icon: "fa-home-lg",
          description:
            "Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia",
        },
        {
          title: "Exclusive",
          icon: "fa-truck",
          description:
            "Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia",
        },
      ],

      invisibleCards: [
        {
          desc: "PLANNING APPLICATIONS",
          count: 3534,
          icon: "fa-folder",
        },
        {
          desc: "COMPLETED PROJECTS",
          count: 896,
          icon: "fa-building",
        },
        {
          desc: "TRAINED PROFESSIONALS",
          count: 172,
          icon: "fa-users",
        },
        {
          desc: "INTERNATIONAL OFFICES",
          count: 19,
          icon: "fa-globe",
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