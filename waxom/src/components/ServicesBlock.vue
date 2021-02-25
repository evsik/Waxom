<template>
  <div class="b-servicesBlock container site_padding">
    <article class="b-designArticle">
      <img src="../assets/icon.svg" alt="design" class="b-designArticle__img">
      <h4 class="b-designArticle__head">
        Web & App Design
      </h4>
      <p class="b-designArticle__text">
        Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim.
      </p>
      <div class="b-designArticle__underline">
      </div>
    </article>
    <article class="b-developArticle">
      <img src="../assets/icon2.svg" alt="design" class="b-developArticle__img">
      <h4 class="b-developArticle__head">
        Development
      </h4>
      <p class="b-developArticle__text">
        Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim.
      </p>
      <div class="b-developArticle__underline">
      </div>
    </article>
    <article class="b-customArticle">
      <img src="../assets/icon3.svg" alt="design" class="b-customArticle__img">
      <h4 class="b-customArticle__head">
        Customization
      </h4>
      <p class="b-customArticle__text">
        Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim.
      </p>
      <div class="b-customArticle__underline">
      </div>
    </article>
    <article class="b-marketArticle">
      <img src="../assets/icon4.svg" alt="market" class="b-marketArticle__img">
      <h4 class="b-marketArticle__head">
        Marketing
      </h4>
      <p class="b-marketArticle__text">
        Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim.
      </p>
      <div class="b-marketArticle__underline">
      </div>
    </article>
  </div>
</template>

<script>
export default {
name: "ServicesBlock"
}
</script>

<style lang="scss">
@import "../layout/styles/_variablesColors";
@import "../layout/styles/_vars";
@import '../../node_modules/bootstrap/scss/bootstrap.scss';
@import '../../node_modules/bootstrap-vue/src/index.scss';

.b-servicesBlock {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 30px;
  text-align: center;
  align-items: end;

  @include media-breakpoint-down(md) {
    grid-template-columns: repeat(2, 1fr);
  }

  @include media-breakpoint-down(sm) {
    grid-template-columns: 1fr;
  }
}

.b-designArticle {

  &:hover div, &:hover h4 {
    opacity: 1;
    color: $varColorHover;
  }

  img {
    margin-bottom: 20px;
  }

  h4 {
  }

  p {
    margin-bottom: 20px;
  }

  div {
    width: 70px;
    height: 3px;
    background-color: $varColorHover;
    display: inline-block;
    opacity: 0;
  }
}

.b-developArticle {
  @extend .b-designArticle;

  img {
    @extend .b-designArticle;
  }

  h4 {
  }

  p {
  }

  div {
    @extend .b-designArticle;
  }
}

.b-customArticle {
  @extend .b-designArticle;

  img {
    @extend .b-designArticle;
  }

  h4 {
  }

  p {
  }

  div {
    @extend .b-designArticle;
  }
}

.b-marketArticle {
  @extend .b-designArticle;

  img {
    @extend .b-designArticle;
  }

  h4 {
  }

  p {
  }

  div {
    @extend .b-designArticle;
  }
}

</style>