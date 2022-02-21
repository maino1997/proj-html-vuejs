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
    <div class="partner-jumbotron">
      <div class="container-strict">
        <div class="row gx-5">
          <div class="col-8">
            <h2 id="building">BUILDING INSPIRING SPACES</h2>
            <div class="yellow-bar"></div>
            <p>
              Vivamus Sed Consectetur Tellus Dolor Sit Amet, Consectetur
              Adipiscing Lorem Elit Sadip Ipsum Ets Ficilis Uns.
            </p>
          </div>
          <div class="col-4">
            <YellowButton ButtonText="GET A FREE QUOTE" />
            <p id="seconds">Only takes a few seconds!</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Title from "./Title.vue";
import PartnerCard from "./PartnerCard.vue";
import YellowButton from "./YellowButton.vue";

export default {
  name: "PartnerSection",
  components: {
    Title,
    PartnerCard,
    YellowButton,
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
.partner-jumbotron {
  background-image: url("../assets/bottom-jumbotron.jpg");
  padding-top: 200px;
  padding-bottom: 90px;
  background-position: center bottom;
  background-size: cover;
}
h2,
p {
  color: white;
  margin-top: 30px;
  margin-bottom: 30px;
}

p {
  font-size: 20px;
}

#building {
  font-weight: 800;
  letter-spacing: 2px;
  font-size: 32px;
}

#seconds {
  font-size: 15px;
  font-weight: 500;
}
</style>