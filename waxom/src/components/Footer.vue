<template>
  <footer>
    <div class="b-footerContentWrapper site_padding container">
      <div class="b-aboutWaxomArticle">
        <div class="b-logo">
          <img src="../assets/logos.svg" alt="logo" class="b-logo__img">
          <h2 class="b-logo__head">
            Waxom
          </h2>
        </div>
        <p class="b-aboutWaxomArticle__text">
          Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut
          laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci suscipit
          lobortis claritatem.
        </p>
        <a href="#" class="b-aboutWaxomArticle__link">
          Read More >
        </a>
      </div>
      <article class="b-recentPosts">
        <h4 class="b-recentPosts__head">
          Recent Posts
        </h4>
        <div class="b-post">
          <h6 class="b-post__data">
            September 08, 2015
          </h6>
          <div class="b-post__text">
            Lorem ipsum dolor sit amet, consectetuer adipiscing elit
          </div>
        </div>
        <div class="b-post b-post_active">
          <h6 class="b-post__data">
            September 08, 2015
          </h6>
          <div class="b-post__text">
            Diam nonummy nibh euismod tincidunt ut laoreet dolore magna
          </div>
        </div>
        <div class="b-post">
          <h6 class="b-post__data">
            September 08, 2015
          </h6>
          <div class="b-post__text">
            Claritas est etiam processus dynamicus, qui sequitur mutationem per seacula quarta decima
          </div>
        </div>
      </article>
      <article class="b-liveTwitter">
        <h4 class="b-liveTwitter__head">
          Our Twitter
        </h4>
        <div class="b-twitterPost">
          <p class="b-twitterPost__text">
            <span>@waxom</span> Cum soluta nobis eleifend option congue nihil imperdiet doming
          </p>
          <p class="b-twitterPost__data">
            3 mins ago
          </p>
        </div>
        <div class="b-twitterPost">
          <p class="b-twitterPost__text">
            Mirum est <span>#envato</span> notare quam littera gothica, quam nunc putamus parum anteposuerit
            litterarum
          </p>
          <p class="b-twitterPost__data">
            5 mins ago
          </p>
        </div>
        <div class="b-twitterPost">
          <p class="b-twitterPost__text">
            Soluta nobis option <a href="#">bit.ly/1Hniso7</a>
          </p>
          <p class="b-twitterPost__data">
            6 mins ago
          </p>
        </div>
      </article>
      <article class="b-dribbleWidget">
        <h4 class="b-dribbleWidget__head">
          Dribbble Widget
        </h4>
        <div class="b-dribbleWidget__wrapperForImg">
          <img src="../assets/widget1.jpg" alt="widget" class="b-dribbleWidget__img">
          <img src="../assets/widget2.jpg" alt="widget" class="b-dribbleWidget__img">
          <img src="../assets/widget3.jpg" alt="widget" class="b-dribbleWidget__img">
          <img src="../assets/widget4.jpg" alt="widget" class="b-dribbleWidget__img">
        </div>
      </article>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer"
}
</script>

<style lang="scss">
@import "../layout/styles/_variablesColors";
@import "../layout/styles/_vars";
@import '../../node_modules/bootstrap/scss/bootstrap.scss';
@import '../../node_modules/bootstrap-vue/src/index.scss';

footer {
  flex-shrink: 0;
  background-color: #191919;
}

.b-footerContentWrapper {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 30px;
  text-align: center;

  align-items: flex-start;

  @include media-breakpoint-down(md) {
    grid-template-columns: repeat(2, 1fr);
  }

  @include media-breakpoint-down(sm) {
    grid-template-columns: 1fr;
  }
}

.b-aboutWaxomArticle {
  text-align: left;

  .b-aboutWaxomArticle__text {
    color: $varColorFooterText;
    font-family: $varFontFamilyMontserratLight;
    line-height: 24px;
    margin-bottom: 30px;
    margin-top: 30px;
    font-size: 14px;
  }

  .b-aboutWaxomArticle__link {
    color: #d1d1d1;
    font-family: $varFontFamilyMontserratRegular;
    font-size: 14px;
    line-height: 20px;
    text-align: left;
  }

}

.b-recentPosts {
  text-align: left;

  .b-recentPosts__head {
    color: $varColorWhite;
    font-family: $varFontFamilyRalewayBold;
    font-size: 24px;
    margin-bottom: 30px;
    margin-top: 30px;
  }
}

.b-post {
  margin-bottom: 30px;

  .b-post__data {
    color: #363636;
    font-family: $varFontFamilyMontserratLight;
    font-size: 12px;
    line-height: 20px;
  }

  .b-post__text {
    color: $varColorFooterText;
    font-family: $varFontFamilyMontserratLight;
    font-size: 14px;
  }
}

.b-post_active {
  .b-post__data {
    color: $varColorWhite;
    font-family: $varFontFamilyMontserratLight;
    font-size: 12px;
    line-height: 20px;
  }

  .b-post__text {
    color: $varColorHover;
    font-family: $varFontFamilyMontserratLight;
    font-size: 14px;
  }
}

.b-liveTwitter {
  @extend .b-recentPosts;

  .b-liveTwitter__head {

    @extend .b-recentPosts__head;
  }
}

.b-twitterPost {
  @extend .b-post;

  .b-twitterPost__text {
    @extend .b-post__text;
    margin-bottom: 0;

    a {
      color: #959595;
    }

    span {
      color: #00bff3;
    }
  }

  .b-twitterPost__data {

    @extend .b-post__data;
    color: #363636;
  }
}

.b-dribbleWidget {
  @extend .b-recentPosts;

  .b-dribbleWidget__head {
    @extend .b-recentPosts__head;

  }

  .b-dribbleWidget__wrapperForImg {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-gap: 10px;

    .b-dribbleWidget__img {
      width: 100%;
    }
  }
}

</style>