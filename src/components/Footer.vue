<template>
  <footer>
    <div class="container">
      <!-- Footer Top  -->
      <div class="row footer-top">
        <!-- First Col  -->
        <div class="col-3">
          <img
            src="https://avada.theme-fusion.com/construction/wp-content/uploads/sites/55/2017/02/footer-logo.png"
            alt="logo"
          />
          <p id="specialist">
            We are specialists in the construction of unique and exclusive
            properties. Our work inspires. We pride ourselves on delivering
            outstanding quality and design for leading clients across the world.
          </p>
          <YellowButton ButtonText="LEARN MORE" />
        </div>

        <!-- Second Col  -->
        <div class="col-3">
          <h3>LATEST TWEET</h3>
          <div class="twitter">
            <img src="../assets/small-logo.png" alt="logo" id="small-logo" />
            <div class="title">
              <h6>Theme Fusion</h6>
              <div id="twitter-ref">@Theme_Fusion</div>
            </div>
          </div>
          <p class="twitter-desc">
            With <span>#Avada</span>, you can build an online #Marketing
            powerhouse website that will drive leads & sales from scratch. For a
            faster turnaround, here are 10 prebuilt one-page websites to import
            at the click of a button
            <span
              >https://bit.ly/3pDih73 #WordPress #wordpresswebsite #HowTo</span
            >
          </p>
          <img src="../assets/footer.jpeg" alt="twiterr" id="twitter-img" />
          <div class="icons text-white">
            <div class="ic">
              <span><i class="bi bi-heart"></i></span>
              <span><i class="bi bi-share"></i></span>
            </div>
            <span>22h</span>
          </div>
        </div>

        <!-- Third Col  -->
        <div class="col-3">
          <h3 id="contact">CONTACT US TODAY</h3>
          <div
            class="footer-address"
            v-for="date in footerContacts"
            :key="date.text"
          >
            <span><i class="bi" :class="date.icon"></i></span>
            <p class="desc">
              {{ date.text }}
            </p>
          </div>
        </div>

        <!-- Fourth Col  -->
        <div class="col-3">
          <h3>OUR LOCATION</h3>
          <!-- <div class="map">
            <YellowButton ButtonText="Find Us" />
          </div> -->
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d153836.1560726705!2d-1.310139122734894!3d52.95400191528019!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x487832d2390779cd%3A0x108063201919db15!2sNottingham%2C%20Regno%20Unito!5e0!3m2!1sit!2sit!4v1646157536908!5m2!1sit!2sit"
            width="600"
            height="450"
            style="border: 0"
            allowfullscreen=""
            loading="lazy"
          ></iframe>
        </div>
      </div>
    </div>
    <FooterBottom :rights="rights" />
  </footer>
</template>

<script>
import YellowButton from "./YellowButton.vue";
import FooterBottom from "./FooterBottom.vue";

export default {
  name: "Footer",
  components: {
    YellowButton,
    FooterBottom,
  },
  props: ["footerContacts", "rights"],
};
</script>

<style scoped lang="scss">
@import "../sass/vars.scss";

footer {
  background-color: rgb(31, 31, 31);
  padding-top: 80px;
  .footer-top {
    padding-bottom: 80px;
  }
}

#specialist {
  color: rgb(116, 116, 116);
  margin-top: 40px;
  line-height: 34.05px;
  font-size: 15px;
}

h3 {
  color: $my-yellow;
  font-size: 16px;
}

.twitter {
  color: white;
  display: flex;
  font-size: 12px;
  margin-top: 40px;
  #small-logo {
    border-radius: 50%;
    width: 40px;
    height: 40px;
  }
  h6 {
    font-size: 12px;
    font-weight: bolder;
  }
}
.twitter-desc {
  font-size: 12px;
  color: white;
  span {
    color: #2970a7;
  }
}

#twitter-img {
  border-radius: 5px;
  margin-bottom: 10px;
}

.icons i {
  margin-left: 10px;
}

.icons {
  display: flex;
  justify-content: space-between;
}

.bi-share {
  margin-right: 150px;
}

#contact {
  margin-bottom: 30px;
}

.footer-address {
  max-width: 250px;
  display: flex;
  font-size: 14px;
  line-height: 23px;
  margin-top: 5px;
  .bi {
    margin-right: 10px;
  }
}

.footer-address {
  color: rgb(116, 116, 116);
}

iframe {
  margin-top: 70px;
  background-color: black;
  width: 350px;
  height: 250px;
  display: flex;
  justify-content: center;
  align-items: center;
}

#map {
  margin-top: 30px;
}
</style>