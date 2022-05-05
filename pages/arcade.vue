<template>
    <section>
        <div class="page-container">
            <header-page />
            <div class="body-container">
                <arcade-body-page />
                <footers-page :hide="hide" />
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