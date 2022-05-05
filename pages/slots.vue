<template>
 <section>
    <div class="page-container">
        <header-page />
        <div class="body-container pr-top-10">
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
   
</style>