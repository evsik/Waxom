<template>
  <main>
    <Slider></Slider>

    <ServicesBlock></ServicesBlock>
  </main>
</template>

<script>
import Slider from "@/components/Slider";
import ServicesBlock from "@/components/ServicesBlock";

export default {
  name: 'Home',
  components: {
    Slider,
    ServicesBlock
  }
}
</script>

<style lang="scss">
@import "../layout/styles/_variablesColors";
@import "../layout/styles/_vars";
@import '../../node_modules/bootstrap/scss/bootstrap.scss';
@import '../../node_modules/bootstrap-vue/src/index.scss';

main {
  flex-grow: 1;
}

</style>
