<template>
  <header>
    <div class="container">
      <nav class="b-nav">
        <div class="b-logo">
          <img src="../assets/logos.svg" alt="logo" class="b-logo__img">
          <h2 class="b-logo__head">
            Waxom
          </h2>
        </div>
        <!--        <slot name="nav"></slot>-->
        <nav class="b-menu" id="nav">
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
        <!--        <nav class="b-menu">-->
        <!--          <ul class="b-menu__ul">-->
        <!--            <li class="b-menu__list">-->
        <!--              <a href="" class="b-menu__link">-->
        <!--                Home-->
        <!--              </a>-->
        <!--            </li>-->
        <!--            <li class="b-menu__list">-->
        <!--              <a href="" class="b-menu__link">-->
        <!--                About Us-->
        <!--              </a>-->
        <!--            </li>-->
        <!--            <li class="b-menu__list">-->
        <!--              <a href="" class="b-menu__link">-->
        <!--                Portfolio-->
        <!--              </a>-->
        <!--            </li>-->
        <!--            <li class="b-menu__list">-->
        <!--              <a href="" class="b-menu__link">-->
        <!--                Features-->
        <!--              </a>-->
        <!--            </li>-->
        <!--            <li class="b-menu__list">-->
        <!--              <a href="" class="b-menu__link">-->
        <!--                Blog-->
        <!--              </a>-->
        <!--            </li>-->
        <!--            <li class="b-menu__list">-->
        <!--              <a href="" class="b-menu__link">-->
        <!--                Pricing-->
        <!--              </a>-->
        <!--            </li>-->
        <!--            <li class="b-menu__list">-->
        <!--              <a href="" class="b-menu__link">-->
        <!--                Shortcodes-->
        <!--              </a>-->
        <!--            </li>-->
        <!--            <li class="b-menu__list">-->
        <!--              <a href="" class="b-menu__link">-->
        <!--                Contact-->
        <!--              </a>-->
        <!--            </li>-->
        <!--          </ul>-->
        <!--        </nav>-->
      </nav>
    </div>
  </header>
</template>

<script>

export default {
  name: "Header",

  watch: {
    '$route': function () {

    },
  }
}

</script>

<style lang="scss">
@import "../layout/styles/_variablesColors";
@import "../layout/styles/_vars";
@import '../../node_modules/bootstrap/scss/bootstrap.scss';
@import '../../node_modules/bootstrap-vue/src/index.scss';

header {
  width: 100%;
  position: absolute;
  z-index: 10;
  padding-top: 20px;
}

.header-background {
  background: url("../assets/header-background.jpg") no-repeat center center;
  background-size: cover;
  height: 50vw;

  @include media-breakpoint-down(sm) {
    height: 400px;
  }
}

.b-nav {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;

  @include media-breakpoint-down(sm) {
    justify-content: space-evenly;
  }
}

.b-logo {
  display: flex;

  @include media-breakpoint-down(sm) {
    align-self: baseline;
  }

  .b-logo__img {
  }

  .b-logo__head {
    font-family: $varFontFamilyRalewayRegular;
    font-size: 34px;
    margin: 0;
    align-self: center;
    color: $varColorWhite;

    @include media-breakpoint-down(md) {
      font-size: 26px;
    }
  }
}

.b-menu {
  align-self: flex-end;

  .b-menu__ul {
    list-style-type: none;
    display: flex;

    @include media-breakpoint-down(sm) {
      flex-direction: column;
    }

    .b-menu__list {
      margin-right: 30px;

      @include media-breakpoint-down(lg) {
        margin-right: 15px;
      }

      .b-menu__link {
        display: inline-block;
        color: $varColorWhite;
        font-family: $varFontFamilyMontserratLight;
        font-size: 14px;
        text-decoration: none;
        transition: 0.6s;

        &:hover {
          transform: scale(1.1);
          color: $varColorHover;
        }

        @include media-breakpoint-down(md) {
          font-size: 11px;
        }
      }

      &:last-of-type {
        margin-right: 0;
      }
    }
  }
}

</style>