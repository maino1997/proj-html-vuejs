<template>
  <div class="footer-bottom">
    <div class="container">
      <div class="content">
        <ul class="d-flex">
          <li><a href="#">©COPYRIGHT 2012 - 2022 |</a></li>
          <li><a href="#">AVADA THEME BY THEMEFUSION |</a></li>
          <li><a href="#"> ALL RIGHTS RESERVED |</a></li>
          <li><a href="#"> POWERED BY WORDPRESS</a></li>
        </ul>
        <ul class="d-flex">
          <li>
            <a href="#"><i class="bi bi-facebook"></i></a>
          </li>
          <li>
            <a href="#"><i class="bi bi-twitter"></i></a>
          </li>
          <li>
            <a href="#"><i class="bi bi-youtube"></i></a>
          </li>
          <li>
            <a href="#"><i class="bi bi-instragram"></i></a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterBottom",
};
</script>

<style scoped lang="scss">
.footer-bottom {
  background-color: black;
  color: rgb(116, 116, 116);
  height: 70px;
}

.container {
  height: 100%;
}

.content {
  justify-content: space-between;
  display: flex;
  height: 100%;
}

ul {
  height: 100%;
  font-size: 12px;
  li {
    height: 100%;
    margin-right: 5px;
  }
}
a {
  display: flex;
  align-items: center;
  color: rgb(116, 116, 116);
  height: 100%;
}
</style>
