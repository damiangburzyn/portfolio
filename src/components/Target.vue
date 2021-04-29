<template>
  <section class="targets" id="targets">
    <div class="cards">
      <div class="crd">
        <div class="card">
          <div class="card__content">
            <h2>Technologie które znam</h2>
            <ul>
              <li>C#</li>
              <li>.NetCore</li>
              <li>Vue.JS</li>
              <li>Umbraco</li>
              <li>Microsoft Sql Server</li>
              <li>MVC</li>
              <li>Entity Framework</li>
              <li>ADO.NET</li>
              <li>Kendo</li>
              <li>WCF</li>
              <li>IBM Websphere MQ</li>
            </ul>
          </div>
        </div>
      </div>
      <div class="crd">
        <div class="card">
          <div class="card__content">
            <h2>Co lubię</h2>
            <p>
              Lubię ciekawe projekty. Problemy których rozwiązywanie przynosi mi
              satysfakcję. Godziny czasu spędzanego nad kodem które dają nowe
              umiejętności.
            </p>
          </div>
        </div>
      </div>
      <div class="crd">
        <div class="card">
          <div class="card__content">
            <h2>Czego chcę się nauczyc</h2>
            <ul>
              <li>Azure</li>
              <li>TDD</li>
              <li>Kolejkowanie</li>
              <li>Angular.JS</li>
            </ul>
            <p>
              Są to technologie z którymi miałem styczność, ale czuję, że
              powinienem w tym kierunku się rozwijać.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Target'
});
</script>

<style lang="scss" scoped>
@import "../sass/mixins.scss";
@include global-reset;
@include disable-text-select("*");
.targets {
  display: flex;
  justify-content: center;
  min-height: 100vh;
  background: black;
  position: relative;
}

.cards {
  position: relative;
  display: flex;
  min-width: 70%;
  flex-wrap: wrap;
  padding: 0 20px;
  @include landscape {
    height: auto;
    align-self: center;
  }
}

.crd {
  position: relative;
  margin: 20px auto;
  min-width: 100%;
  transition: 0.5s;

  //Flex box the same width for each column
  flex-grow: 1;
  flex-basis: 0;
  @include landscape {
    min-width: auto;
  }

  &:nth-child(2) .card::before,
  &:nth-child(2) .card::after {
    background: linear-gradient(315deg, #03a9f4, #ff0058);
  }

  &:nth-child(3) .card::before,
  &:nth-child(3) .card::after {
    background: linear-gradient(315deg, #4dff03, #03a9f4);
  }
}

.card {
  position: relative;
  height: 100%;
  transition: 0.5s;

  &:hover {
    transform: translateY(-20px);
  }

  &::before {
    content: "";
    position: absolute;
    z-index: 9;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(45deg, #ffbc00, #ff0058);
  }

  &::after {
    content: "";
    position: absolute;
    z-index: 9;
    top: 0;
    left: -2%;
    width: 100%;
    height: 100%;
    padding-left: 20px;
    background: linear-gradient(45deg, #ffbc00, #ff0058);
    filter: blur(20px);
  }

  @include landscape {
    min-width: auto;
    margin: 10px;
  }

  &__content {
    color: white;
    position: relative;
    height: 100%;
    z-index: 10;
    padding: 20px 30px;

    &::before {
      content: "";
      background-color: rgba(0, 0, 0, 0.5);

      margin: 4px 4px;
      position: absolute;
      z-index: -1;
      top: 0;
      left: 0;
      bottom: 0;
      right: 0;
    }
  }

  ul {
    list-style-type: disc;
    li {
      margin-left: 20px;
      text-align: left;
    }
  }
}
</style>