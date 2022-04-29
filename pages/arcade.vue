<template>
    <section>
        <div class="page-container">
            <header-page />
            <div class="body-container">
                <arcade-body-page />
                <footers-page />
            </div>
        </div> 
    </section>
</template>

<script>
    export default {
        components: {
            HeaderPage: () => import('../components/page/HeaderPage'),
            ArcadeBodyPage: () => import('../components/page/ArcadeBodyPage'),
            FootersPage: () => import('../components/page/FootersPage')
        }
    }
</script>

<style lang="scss" amp-boilerplate>
    .page-container {
        .body-container {
        @extend .container-size;
        @extend .magrin-0-auto;
        }
    }
</style>