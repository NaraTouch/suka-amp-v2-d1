<template>
  <section>
    <div class="page-container">
        <header-page />
        <div class="body-container">
          <index-body-page />
          <footers-page />
        </div>
    </div> 
  </section>
</template>

<script>
  export default {
    components: {
      HeaderPage: () => import('../components/page/HeaderPage'),
      IndexBodyPage: () => import('../components/page/IndexBodyPage'),
      FootersPage: () => import('../components/page/FootersPage'),
    },
  }
</script>

<style lang="scss">
  .page-container {
     .body-container {
        @extend .container-size;
        margin: 0 auto;
     }
  }
</style>