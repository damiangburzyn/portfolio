<template>
  <!-- <style src='./assets/fonts/fontawesome/all.css'></style> -->
  <!-- <teleport to="head">
  <link href="/assets/fonts/fontawesome/all.css" rel="stylesheet"/>
    </teleport> -->
  <section class="contact">
    <div class="contact__content">
      <div class="title">
        <img src="../assets/me.jpg" alt="me" />
        <h3>Kontakt:</h3>
      </div>
      <!--
<ul>
  <li class="email">damian.gburzyn@gmail.com</li>
  <li></li>
  <li></li>
  <li></li>
</ul> -->

      <div class="email">
        <i class="far fa-envelope"></i> <span> damian.gburzyn@gmail.com</span>
      </div>
      <div class="phone">
        <i class="fas fa-mobile-alt"></i> <span>+48 729 245 367</span>
      </div>
      <div class="facebook">
        <i class="fab fa-facebook"></i> <a href="https://www.facebook.com/damian.gburzynski.7">Damian Gburzyński</a>
      </div>
      <div class="linked-in">
        <i class="fab fa-linkedin"></i> <a href="https://www.linkedin.com/in/damian-gburzy%C5%84ski-695647194/">Damian Gburzyński</a>
      </div>
    </div>
  </section>
</template>





<style lang="scss" scoped>
@import "../sass/mixins.scss";

@include global-reset;
@include disable-text-select("*");

.contact {
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  background-color: #1c1d25;

  &__content{
  max-width: 400px;
  margin:auto;
  h3 {
    margin-top: 20px;
  }
  img {
    clip-path: circle(50%);
    width: 80px;
  }

  ul {
    justify-content: center;
    display: flex;
  }

  div {
    margin-top: 10px;
    position: relative;
    span {
      line-height: 40px;
    }
    i {
      font-size: 40px;

       @include min-width(370px) {
         position: absolute;
      }
      display: block;
      top: 0;
      left: 10px;
    }
    a {
      text-decoration: none;
      color: #fff;
      line-height: 40px;
    }
  }
  }
}
</style>