<template>
    <section>
        <div class="page-container">
            <header-page />
            <div class="body-container">
                <hot-game-body-page />
                <footers-page />
            </div>
        </div> 
    </section>
</template>

<script>
    export default {
        components: { 
            HeaderPage: () => import('../components/page/HeaderPage'),
            HotGameBodyPage: () => import('../components/page/HotGameBodyPage'), 
            FootersPage: () => import('../components/page/FootersPage'),
        },
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