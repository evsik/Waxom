<template>
  <h5 id="about">
    ЖОПА
  </h5>
</template>

<script>
import Header from "@/components/Header";

export default {
  name: "About",
  components: Header,

  mounted() {
    this.customStyle()
  },
  methods: {
    customStyle() {
      if (document.querySelector("header")){
        document.querySelector("header").style.backgroundColor = "#3996f5";
      }
    }
  },
  // computed: {
  //   function() {
  //     if (this.$route.path === '/about'){
  //       this.customStyle()
  //     }
  //   }
  // }
}
</script>

<style lang="scss">

//#about {
//
//}

</style>