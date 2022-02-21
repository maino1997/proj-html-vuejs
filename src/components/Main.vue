<template>
  <main>
    <!-- Jumbotron Top  -->
    <div class="jumbotron-top">
      <div class="container-strict">
        <div class="row">
          <div
            class="col-12 d-flex justify-content-center flex-column text-center"
          >
            <h1>BUILDING INSPIRING SPACES</h1>
            <h4>We Build Inspiring Residential & Commercial Spaces</h4>
            <div class="buttons">
              <BlackButton ButtonText="Explore Recent Work" />
              <YellowButton ButtonText="Get Quote" />
            </div>
          </div>
        </div>
      </div>
      <div class="yellow-light">
        <h3>Do You Have A Construction Project We Can Help With?</h3>
        <BlackButton ButtonText="Get a Free Quote" id="bottom-black-button" />
      </div>
    </div>

    <!-- Works Section  -->

    <WorksSection :showCards="showCards" />
    <ValueSection :showCards="showCards" />
    <PartnerSection />
  </main>
</template>

<script>
import YellowButton from "./YellowButton.vue";
import BlackButton from "./BlackButton.vue";
import WorksSection from "./WorksSection.vue";
import ValueSection from "./ValueSection.vue";
import PartnerSection from "./PartnerSection.vue";

export default {
  name: "Main",
  components: {
    YellowButton,
    BlackButton,
    WorksSection,
    ValueSection,
    PartnerSection,
  },
  data() {
    return {
      showCards: [
        {
          url1: require("../assets/seconda.jpg"),
          url2: require("../assets/quarta.jpg"),
          title: "Redeveloping Florida’s Remote Southern Coast",
          description:
            "Technology is Here to Stay Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus purus nisl, elementum vitae consequat at, tristique ut enim. Sed ut dignissim leo. Nullam sed metus id sapien faucibus rhoncus sed",
          date: "December 7th, 2015",
          hoverTitle: "Florida Health Facility",
          hoverTextUp: "Commercial",
          hoverTextDown: "Architecture, Buildings, Constructions, News",
        },
        {
          url1: require("../assets/prima.jpg"),
          url2: require("../assets/quinta.jpg"),
          title: "How We Manage Large Construction Projects",
          description:
            "Technology is Here to Stay Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus purus nisl, elementum vitae consequat at, tristique ut enim. Sed ut dignissim leo. Nullam sed metus id sapien faucibus rhoncus sed",
          date: "December 7th, 2015",
          hoverTitle: "Maine Modernity",
          hoverTextUp: "Residential",
          hoverTextDown: "Architecture, Construction, Engineering",
        },
        {
          url1: require("../assets/terza.jpg"),
          url2: require("../assets/sesta.jpg"),
          title: "Future proofing a modern home",
          description:
            "Technology is Here to Stay Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus purus nisl, elementum vitae consequat at, tristique ut enim. Sed ut dignissim leo. Nullam sed metus id sapien faucibus rhoncus sed",
          date: "December 6th, 2015",
          hoverTitle: "Exclusive Urban Living",
          hoverTextUp: "Commercial",
          hoverTextDown: "Architecture, Construction, Marketing",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../sass/vars.scss";

main {
  padding-top: 140px;
}

.jumbotron-top {
  background-image: url("https://avada.theme-fusion.com/construction/wp-content/uploads/sites/55/2015/12/home-slider-62528242.jpg");
}
h1 {
  font-weight: bolder;
  color: white;
  font-size: 3.5rem;
  margin-top: 150px;
  margin-bottom: 40px;
}

h4 {
  color: $my-yellow;
  margin-bottom: 30px;
}

button {
  margin-bottom: 200px;
  margin-right: 20px;
}

.yellow-light {
  background-color: $my-yellow;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 50px 0;
  position: relative;
  #bottom-black-button {
    position: absolute;
    top: 120px;
  }
}
</style>