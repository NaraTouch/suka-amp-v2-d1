<template>
    <section>
        <div class="page-container">
            <header-page />
            <div class="body-container">
                <cock-fighter-body-page />
                <footers-page />
            </div>
        </div> 
    </section>
</template>

<script>
    export default {
        components: {
            HeaderPage: () => import('../components/page/HeaderPage'),
            CockFighterBodyPage: () => import('../components/page/CockFighterBodyPage'),
            FootersPage: () => import('../components/page/FootersPage')
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