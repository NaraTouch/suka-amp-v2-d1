<template>
    <section>
        <div class="page-container">
            <header-page />
            <div class="body-container">
                <!-- <sports-body-page /> -->
                <casino-body-page />
                <footers-page :hide="hide" />
            </div>
        </div> 
    </section>
</template>

<script>
    export default {
        components: {
            HeaderPage: () => import('../components/page/HeaderPage'),
            CasinoBodyPage: () => import('../components/page/CasinoBodyPage'),
            // SportsBodyPage: () => import('../components/page/SportsBodyPage'),
            FootersPage: () => import('../components/page/FootersPage'),
        },
        data() {
            return {
                hide: true,
            }
        },
    }
</script>

<style lang="scss">
    .page-container {
        .body-container {
        @extend .container-size;
        @extend .magrin-0-auto;
        }
    }
</style>