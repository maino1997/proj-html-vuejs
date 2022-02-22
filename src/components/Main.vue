<template>
  <main>
    <!-- Fixed Right Elements  -->
    <div class="fixed-right" id="first">
      <i class="bi bi-handbag-fill"></i>
      <p class="text-dark">Demons</p>
    </div>
    <div class="fixed-right" id="second">
      <p id="g">$ 39</p>
      <p>Buy Now</p>
    </div>

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
              <BlackButton ButtonText="EXPLORE RECENT WORK" />
              <YellowButton ButtonText="GET A QUOTE TODAY" />
            </div>
          </div>
        </div>
      </div>

      <!-- Yellow Bar  -->
      <div class="yellow-light">
        <h3>Do You Have A Construction Project We Can Help With?</h3>
        <BlackButton ButtonText="GET A FREE QUOTE" id="bottom-black-button" />
      </div>
    </div>

    <!-- Sections  -->
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
          url2: require("../assets/quinta.jpg"),
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
          url2: require("../assets/quarta.jpg"),
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
  padding-top: 138px;
}

.jumbotron-top {
  background-image: url("../assets/home.jpg");
  background-size: cover;
}

.buttons {
  margin-bottom: 55px;
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
    &:hover {
      color: black;
      background-color: white;
      border: 2px solid black;
    }
  }
}

.fixed-right {
  position: fixed;
  z-index: 2;
  right: 20px;
  background-color: white;
  border-radius: 5px;
  display: flex;
  flex-direction: column;
  align-items: center;
  box-shadow: 0 3px 10px rgb(0 0 0 / 0.2);
  &:hover i {
    animation: iconIn 0.2s linear;
  }
  &:hover {
    cursor: pointer;
  }
  p {
    margin: 0;
    font-size: 12px;
    font-weight: 500px;
  }
  i {
    font-size: 1.5rem;
  }
}

#first {
  top: 160px;
  padding: 8px 10px;
}

#second {
  top: 250px;
  padding: 10px 8px;
}

#g {
  color: green;
  font-size: 18px;
}

@keyframes iconIn {
  0% {
    transform: translate(0);
  }
  50% {
    transform: translate(-120%);
  }
  100% {
    transform: translate(0);
  }
}
</style>