<template>
  <section id="partners">
    <!-- First Block with Carousel Cards  -->
    <div class="container">
      <Title Title="Trusted Partners" :show="true" />
    </div>
    <div class="container-strict card-slider">
      <div class="row">
        <div class="carousel">
          <PartnerCard
            :url="partners[currentIndex].url"
            class="fade-in slider-item"
          />
          <PartnerCard
            :url="partners[secondIndex].url"
            class="fade-in active slider-item"
          />
          <PartnerCard
            :url="partners[thirdIndex].url"
            class="fade-in active slider-item"
          />
          <PartnerCard
            :url="partners[fourthIndex].url"
            class="fade-in active slider-item"
          />
          <PartnerCard
            :url="partners[fitfthIndex].url"
            class="fade-in active slider-item"
          />
        </div>
        <!-- <PartnerCard
          v-for="(card, index) in partners"
          :key="index"
          :url="card.url"
          :card="card"
        /> -->
      </div>
    </div>

    <!-- Jumbotron Partner  -->
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
      currentIndex: 0,
      secondIndex: 1,
      thirdIndex: 2,
      fourthIndex: 3,
      fitfthIndex: 4,
      sixIndex: 5,
    };
  },
  methods: {
    isIndex(index) {
      return index === this.currentIndex;
    },

    newPic(currIndex) {
      if (this[currIndex] === this.partners.length - 1) {
        this[currIndex] = 0;
      } else {
        this[currIndex]++;
      }
    },
  },
  created() {
    setInterval(() => {
      this.newPic("currentIndex");
      this.newPic("secondIndex");
      this.newPic("thirdIndex");
      this.newPic("fourthIndex");
      this.newPic("fitfthIndex");
    }, 3000);
  },
};
</script>

<style scoped lang="scss">
@import "../sass/vars.scss";

section {
  padding-top: 60px;
}

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

.card-slider {
  margin-bottom: 100px;
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

.fade-in {
  transition: 0.5s linear;
}

.yellow-bar {
  height: 1.5px;
  width: 200px;
  background-color: $my-yellow;
}

.carousel {
  width: 1000px;
  margin: auto;
  overflow: hidden;
  display: flex;
  inset: auto, auto, auto -115px;
}

.active {
  animation: fadeIn 2s linear;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>