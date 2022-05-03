<template>
 <section>
    <div class="page-container">
        <header-page />
        <div class="body-container">
            <slots-body-page />
            <footers-page :hide="hide" />
        </div>
    </div> 
  </section>
</template>

<script>
    export default {
        components: {
            SlotsBodyPage: () => import('../components/page/SlotsBodyPage'),
            HeaderPage: () => import('../components/page/HeaderPage'),
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
    .page-container {
        .body-container {
            @extend .container-size;
            @extend .magrin-0-auto;
            padding: 10px 0px;
        }
  }
</style>