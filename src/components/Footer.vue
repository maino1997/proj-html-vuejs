<template>
  <footer>
    <div class="container">
      <div class="row footer-top">
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
            With #Avada, you can build an online #Marketing powerhouse website
            that will drive leads & sales from scratch. For a faster turnaround,
            here are 10 prebuilt one-page websites to import at the click of a
            button https://bit.ly/3pDih73 #WordPress #wordpresswebsite #HowTo
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
        <div class="col-3">
          <h3>CONTACT US TODAY</h3>
          <div class="footer-address">
            <span><i class="bi bi-globe2"></i></span>
            <p class="desc">
              Corporate Location 1600 Amphitheatre Parkway London WC1 1BA
            </p>
          </div>
          <div class="footer-address">
            <span><i class="bi bi-house"></i></span>
            <p class="desc">
              Residential Location 9521 Broadsberry Avenue Paddington RC7 9ZA
            </p>
          </div>
          <div class="footer-address">
            <span><i class="bi bi-telephone"></i></span>
            <p class="desc">1.800.458.556 / 1.800.532.2112</p>
          </div>
          <div class="footer-address">
            <span><i class="bi bi-telephone"></i></span>
            <p class="desc">info@your-domain.com</p>
          </div>
          <div class="footer-address">
            <span><i class="bi bi-clock"></i></span>
            <p class="desc">Monday – Friday: 9:00 AM – 6:00 PM</p>
          </div>
          <div class="footer-address">
            <span><i class="bi bi-clock"></i></span>
            <p class="desc">Saturday – Sunday: 9:00 AM – 12:00 PM</p>
          </div>
        </div>
        <div class="col-3">
          <h3>OUR LOCATION</h3>
          <div class="map">
            <YellowButton ButtonText="Find Us" />
          </div>
        </div>
      </div>
    </div>
    <FooterBottom />
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

.footer-address {
  max-width: 250px;
  display: flex;
  font-size: 14px;
  .bi {
    margin-right: 10px;
  }
}

.footer-address {
  color: rgb(116, 116, 116);
}

.map {
  margin-top: 70px;
  background-color: black;
  width: 350px;
  height: 250px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>