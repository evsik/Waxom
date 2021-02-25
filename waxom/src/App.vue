<template>
  <div id="app">
    <!--    <div id="nav">-->
    <!--      <router-link to="/">Home</router-link> |-->
    <!--      <router-link to="/about">About</router-link>-->
    <!--    </div>-->
    <Header>

    </Header>

    <router-view/>

    <footer/>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Slider from "@/components/Slider";

export default {
  name: "App",
  components: {
    Header,
    Slider
  },
  updated() {
    this.customStyle()
  },
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

//.b-menu {
//  align-self: flex-end;
//
//  .b-menu__ul {
//    list-style-type: none;
//    display: flex;
//
//    .b-menu__list {
//      margin-right: 30px;
//
//      &:hover .b-menu__link {
//        transform: scale(1.1);
//        color: $varColorHover;
//      }
//
//      .b-menu__link {
//        display: inline-block;
//        color: $varColorWhite;
//        font-family: $varFontFamilyMontserratLight;
//        font-size: 14px;
//        text-decoration: none;
//        transition: 0.6s;
//
//        @include media-breakpoint-down(md) {
//          font-size: 11px;
//        }
//      }
//
//      &:last-of-type {
//        margin-right: 0;
//      }
//
//      @include media-breakpoint-down(lg) {
//        margin-right: 15px;
//      }
//    }
//
//    @include media-breakpoint-down(sm) {
//      flex-direction: column;
//    }
//  }
//}

</style>
