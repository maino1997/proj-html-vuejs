<template>
  <section id="partners">
    <div class="container">
      <Title Title="Trusted Partners" />
    </div>
    <div class="container-strict">
      <div class="row">
        <PartnerCard
          v-for="(card, index) in partners"
          :key="index"
          :url="card.url"
        />
      </div>
    </div>
  </section>
</template>

<script>
import Title from "./Title.vue";
import PartnerCard from "./PartnerCard.vue";

export default {
  name: "PartnerSection",
  components: {
    Title,
    PartnerCard,
  },
  data() {
    return {
      partners: [
        {
          url: require("../assets/partner1.png"),
        },
        {
          url: require("../assets/partner2.png"),
        },
        {
          url: require("../assets/partner3.png"),
        },
        {
          url: require("../assets/partner4.png"),
        },
        {
          url: require("../assets/partner5.png"),
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
</style>