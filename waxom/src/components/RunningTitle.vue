<template>
  <div class="b-runningTitle">
    <div class="b-runningTitle__Wrapper container site_padding">
      <ul class="b-runningTitle__info">
        <li class="b-runningTitle__list">
          <a class="b-runningTitle__link">
            Copyright © 2015 <span>Waxom</span>
          </a>
        </li>
        <li class="b-runningTitle__list">
          <a href="" class="b-runningTitle__link">
            Privacy Policy
          </a>
        </li>
        <li class="b-runningTitle__list">
          <a href="" class="b-runningTitle__link b-runningTitle__link_active">
            FAQ
          </a>
        </li>
        <li class="b-runningTitle__list">
          <a href="" class="b-runningTitle__link">
            Support
          </a>
        </li>
      </ul>
      <ul class="b-runningTitle__info">
        <li class="b-runningTitle__list">
          <a href="" class="b-runningTitle__link">
            Designed by <span>Designed by</span>
          </a>
        </li>
        <li class="b-runningTitle__list">
          <a href="" class="b-runningTitle__link">
            Only on <span>Envato Market</span>
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
name: "RunningTitle"
}
</script>

<style lang="scss">
@import "../layout/styles/_variablesColors";
@import "../layout/styles/_vars";
@import '../../node_modules/bootstrap/scss/bootstrap.scss';
@import '../../node_modules/bootstrap-vue/src/index.scss';

.b-runningTitle {
  background-color: #111111;

  .b-runningTitle__Wrapper {
    display: flex;
    flex-flow: wrap;
    justify-content: space-between;

    @include media-breakpoint-down(sm) {
      justify-content: center;
    }

    .b-runningTitle__info {
      list-style-type: none;
      display: flex;
      margin-bottom: 0;

      @include media-breakpoint-down(sm) {
        margin-bottom: 15px;
      }

      .b-runningTitle__list {
        margin-right: 10px;

        &:last-of-type {
          margin-right: 0;
        }

        .b-runningTitle__link {
          color: $varColorFooterText;
          font-family: $varFontFamilyMontserratLight;
          font-size: 13px;
          line-height: 20px;
          text-decoration: none;

          @include media-breakpoint-down(sm) {
            font-size: 11px;
          }

          span {
            color: #959595;
          }
        }

        .b-runningTitle__link_active {
          color: $varColorHover;
        }
      }
    }
  }
}

</style>