<template>
  <section class="hero">
    <div class="hero__container">
      <div class="hero__description">
        <div>
          <h1 class="name">Damian Gburzyński</h1>
          <p>Web Developer</p>
          <a href="#" @click.prevent="scrollMeTo('targets')">
            <span></span>
            <span></span>
            <span></span>
            <span></span>
            Więcej ...
          </a>
        </div>
      </div>
      <img class="portrait" alt="Vue logo" src="../assets/hero2.jpg" />
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Hero',
  methods: {
    scrollMeTo(id: string) {
      const element = document.getElementById(id);
      const htElement = (element as HTMLHRElement);
      const top = htElement.offsetTop;
      window.scrollTo({ top: top, behavior: "smooth" });
    }

  }
});
</script>


<style lang="scss" scoped>
@import "../sass/mixins.scss";

@include global-reset;
@include disable-text-select("*");

.hero {
  background-color: #1c1d25;
  color: #fff;

  &__container {
    position: relative;
    width: 100%;
    height: 100vh;
  }

  &__description {
    position: absolute;
    top: 10%;
    margin-left: auto;
    margin-right: auto;
    left: 0;
    right: 0;
    z-index: 1;

    @include landscape {
      display: grid;
      width: 50%;
      height: 100vh;
      right: auto;
      top: auto;
      margin: auto;

      div {
        place-self: center;
      }
    }

    .name {
      font-size: 30px;
      @include min-height(730px) {
        font-size: 35px;
      }
      @include min-width(730px) {
        font-size: 5.3vw;
      }
      @include landscape {
        font-size: 4.3vw;
      }
    }

    p {
      @include min-width(730px) {
        font-size: 30px;
      }
      @include landscape {
        font-size: 2vw;
      }
    }

    a {
      position: relative;
      display: inline-block;
      padding: 15px 30px;
      color: #2196f3;
      text-transform: uppercase;
      letter-spacing: 4px;
      text-decoration: none;
      font-size: 16px;
      overflow: hidden;
      transition: 0.2s;
      margin: 20px 10px 0px 10px;

      @include min-width(360px) {
        margin-top: 10vh;
      }

      @include min-width(730px) {
        font-size: 24px;
      }
      @include landscape {
        font-size: 1.8vw;
      }

      &:hover,  &:active {
        color: #255784;
        background: #2196f3;
        box-shadow: 0 0 10px #2196f3, 0 0 40px #2196f3, 0 0 80px #2196f3;
        transition-delay: 1s;
        span:nth-child(1) {
          left: 100%;
          transition: 1s;
        }

         span:nth-child(2) {

           top: 100%;
          transition: 1s;
          transition-delay: 0.25s;
        }

        span:nth-child(3) {

           right: 100%;
          transition: 1s;
          transition-delay: 0.5s;
        }

        span:nth-child(4) {

          bottom: 100%;
          transition: 1s;
          transition-delay: 0.75s;
        }

      }

span{
  position: absolute;
  display:block
}

      span:nth-child(1) {
        top: 0;
        left: -100%;
        width: 100%;
        height: 2px;
        background: linear-gradient(90deg, transparent, #2196f3);
      }
 span:nth-child(2) {
        top: -100%;
        right: 0%;
        width: 2px;
        height: 100%;
        background: linear-gradient(270deg, transparent, #2196f3);
      }

 span:nth-child(3) {
        bottom: 0;
        right: -100%;
        width: 100%;
        height: 2px;
        background: linear-gradient(180deg, transparent, #2196f3);
      }
 span:nth-child(4) {
        bottom:-100%;
        left: 0;
        width: 2px;
        height: 100%;
        background: linear-gradient(0deg, transparent, #2196f3);
      }
    }
  }
}
.portrait {
  max-width: 100vw;
  max-height: 60vh;
  position: absolute;
  left: 0;
  bottom: 0;

  @include landscape {
    width: auto;
    max-width: 50%;
    max-height: 100%;
    transform: rotateY(180deg);
    left: auto;
    right: 0;
  }
}
</style>