<template>
    <div class="hedaer-page">
        <nav-bar-header />

        <div class="page-size pr-top-10">
            <div class="running-text">
                <running-text />
            </div>

            <div class="navbar-image pr-top-10">
                <nav-image />
            </div>

            <div class="running-image pr-top-10">    
                <running-image />
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        components: {
            NavBarHeader: () => import('../header/NavBarHeader'),
            NavImage: () => import('../body/NavImage'),
            RunningImage: () => import('../RunningImage'),
        }
    }
</script>

<style lang="scss" amp-boilerplate>
    .hedaer-page {
        .page-size {
            @extend .container-size;
            @extend .magrin-0-auto;
            // padding-top: 10px;

            .navbar-image {
                //  padding: 10px 0px;
            }
        }
    }
</style>