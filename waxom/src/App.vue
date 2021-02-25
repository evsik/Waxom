<template>
  <div id="app">
    <Header>
      <nav class="b-menu" id="nav" slot="nav">
        <ul class="b-menu__ul">
          <li class="b-menu__list">
            <router-link class="b-menu__link" to="/">Home</router-link>
          </li>
          <li class="b-menu__list">
            <router-link class="b-menu__link" to="/about">About us</router-link>
          </li>
          <li class="b-menu__list">
            <a href="" class="b-menu__link">
              Portfolio
            </a>
          </li>
          <li class="b-menu__list">
            <a href="" class="b-menu__link">
              Features
            </a>
          </li>
          <li class="b-menu__list">
            <a href="" class="b-menu__link">
              Blog
            </a>
          </li>
          <li class="b-menu__list">
            <a href="" class="b-menu__link">
              Pricing
            </a>
          </li>
          <li class="b-menu__list">
            <a href="" class="b-menu__link">
              Shortcodes
            </a>
          </li>
          <li class="b-menu__list">
            <a href="" class="b-menu__link">
              Contact
            </a>
          </li>
        </ul>
      </nav>
    </Header>

    <router-view/>

    <Footer/>
    <RunningTitle/>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Slider from "@/components/Slider";
import Footer from "@/components/Footer";
import RunningTitle from "@/components/RunningTitle";

export default {
  name: "App",
  components: {
    Header,
    Slider,
    Footer,
    RunningTitle
  },


  updated() {
    this.customStyle()
  },

  //This method will be needed in the future to change the header style when switching the router
  methods: {
    customStyle() {
      if (this.$route.path === '/about') {
        document.querySelector("header").style.backgroundColor = "#3996f5";
      } else {
        document.querySelector("header").style.backgroundColor = "#ffffff";
      }
    }
    // computed: {
    //   changeColor() {
    //     if (this.$route.path === '/about') {
    //       console.log("ghbdtn")
    //     }
    //   }
    // }
  }

}

</script>

<style lang="scss">
@import "./layout/styles/_variablesColors";
@import "./layout/styles/_vars";
@import '../node_modules/bootstrap/scss/bootstrap.scss';
@import '../node_modules/bootstrap-vue/src/index.scss';

#app {
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.b-menu {
  align-self: flex-end;

  .b-menu__ul {
    list-style-type: none;
    display: flex;

    .b-menu__list {
      margin-right: 30px;

      &:hover .b-menu__link {
        transform: scale(1.1);
        color: $varColorHover;
      }

      .b-menu__link {
        display: inline-block;
        color: $varColorWhite;
        font-family: $varFontFamilyMontserratLight;
        font-size: 14px;
        text-decoration: none;
        transition: 0.6s;

        @include media-breakpoint-down(md) {
          font-size: 11px;
        }
      }

      &:last-of-type {
        margin-right: 0;
      }

      @include media-breakpoint-down(lg) {
        margin-right: 15px;
      }
    }

    @include media-breakpoint-down(sm) {
      flex-direction: column;
    }
  }
}

</style>
