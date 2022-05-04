<template>
   <section>
    <div class="page-container">
        <header-page />
        <div class="body-container">
            <sports-body-page />
            <footers-page :hide="hide" />
        </div>
    </div> 
  </section>
</template>

<script>
    export default {
        components: {
            HeaderPage: () => import('../components/page/HeaderPage'),
            SportsBodyPage: () => import('../components/page/SportsBodyPage'),
            FootersPage: () => import('../components/page/FootersPage'),
        },
        data() {
            return {
                hide: true
            }
        },
    }
</script>

<style lang="scss" amp-boilerplate>
    //  .page-container {
    //     .body-container {
    //         @extend .container-size;
    //         @extend .magrin-0-auto;
    //     }
    // }
</style>