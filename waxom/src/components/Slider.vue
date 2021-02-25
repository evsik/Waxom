<template>
  <div class="slider">
<!--    <Header></Header>-->
    <div id="carouselExampleCaptions" class="carousel slide" data-ride="carousel">
      <ol class="carousel-indicators">
        <li data-target="#carouselExampleCaptions" data-slide-to="0" class="active"></li>
        <li data-target="#carouselExampleCaptions" data-slide-to="1"></li>
        <li data-target="#carouselExampleCaptions" data-slide-to="2"></li>
      </ol>
      <div class="carousel-inner">
        <div class="carousel-item header-background active">
          <!--                <img src="images/header-background.jpg" class="d-block w-100" alt="...">-->
          <div class="carousel-caption d-none d-md-block">
            <h5>Portfolio PSD Template</h5>
            <p>Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet
              <br>
              doming id quod mazim
              placerat facer possim assum.</p>
          </div>
        </div>
        <!--            <div class="carousel-item header-background">-->
        <!--                &lt;!&ndash;                <img src="images/header-background.jpg" class="d-block w-100" alt="...">&ndash;&gt;-->
        <!--                <div class="carousel-caption d-none d-md-block">-->
        <!--                    <h5>Second slide label</h5>-->
        <!--                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>-->
        <!--                </div>-->
        <!--            </div>-->
        <!--            <div class="carousel-item header-background">-->
        <!--                &lt;!&ndash;                <img src="images/header-background.jpg" class="d-block w-100" alt="...">&ndash;&gt;-->
        <!--                <div class="carousel-caption d-none d-md-block">-->
        <!--                    <h5>Third slide label</h5>-->
        <!--                    <p>Praesent commodo cursus magna, vel scelerisque nisl consectetur.</p>-->
        <!--                </div>-->
        <!--            </div>-->
      </div>
      <a class="carousel-control-prev" href="#carouselExampleCaptions" role="button" data-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
      </a>
      <a class="carousel-control-next" href="#carouselExampleCaptions" role="button" data-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
      </a>
    </div>
  </div>
</template>

<script>
import Header from "@/components/Header";

export default {
  name: "Slider",
  components: {
    Header
  },
}


</script>

<style lang="scss">
@import "../layout/styles/_variablesColors";
@import "../layout/styles/_vars";
@import '../../node_modules/bootstrap/scss/bootstrap.scss';
@import '../../node_modules/bootstrap-vue/src/index.scss';

.slider {
  position: relative;
}

.carousel-caption {
  top: 30% !important;

  h5 {
    color: $varColorWhite;
    font-family: $varFontFamilyRalewayMedium;
    font-size: 36px;

    @include media-breakpoint-down(md) {
      font-size: 28px;
    }
  }

  p {
    font-family: $varFontFamilyMontserratLight;
    font-size: 16px;
    line-height: 24px;

    @include media-breakpoint-down(md) {
      font-size: 11px;
    }
  }
}

.carousel-control-prev-icon {
  background: url("../assets/left.svg") !important;
  width: 40px !important;
  height: 73px !important;
}

.carousel-control-next-icon {
  background: url("../assets/right.svg") !important;
  width: 40px !important;
  height: 73px !important;
}


</style>