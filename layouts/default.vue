<template>
  <div class="content">
    <!-- <NavBar /> -->
    <Nuxt /> 
  </div>
</template>

<script>
import NavBar from "~/components/NavBar.vue";

export default {
  components: {
    NavBar,
  },
};
</script>
<style lang="scss" amp-boilerplate>
  html {
    font-family:  Arial,"Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
      "Helvetica Neue", sans-serif;
    font-size: 16px;
    word-spacing: 1px;
    -ms-text-size-adjust: 100%;
    -webkit-text-size-adjust: 100%;
    -moz-osx-font-smoothing: grayscale;
    -webkit-font-smoothing: antialiased;
    box-sizing: border-box;
    color: #000;
  }

  *, *:before, *:after {
    box-sizing: border-box;
    margin: 0;
  }
  .content {
    min-height: 100vh;
    background: #000000;
  }
  .container {
    margin: 0 auto;
    padding: 0 10px;
    width: 100%;
  }

  .page-container .body-container {
    width: 1024px;
    margin: 0 auto;
  }

  .pr-top-10 {
    padding: 10px 0px 0px 0px;
  }
</style>
