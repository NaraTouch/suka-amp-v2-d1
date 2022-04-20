<template>
    <div class="running-container">
        <div class="text">
            <title-image :image-title="titleIcon" :width="width" :height="height" />
        </div>
        <div class="marquee-container">
            <div class="marquee d-flex justify-content-around">
                <span>{{ title }}</span>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        components: {
            TitleImage: () => import('../components/TitleImage'),
        },
        data() {
            return {
                titleIcon: "/images/card/running-text-logo.png",
                width: "25",
                height: "20",
                title: "Selamat datang di Sukabet! Silahkan masuk atau daftar jika anda belum memiliki akun. Jadi pemenang berikutnya dan rasakan bermain di Sukabet!"
            }
        },
    }
</script>

<style lang="scss" >
    .running-container {
        @extend .border-radius-3px;
        @extend .display-flex;
        background-color: $bg-gray-contain;

        .text {
            margin: 13px 0px 0px 5px;
            
            span {
                svg{ 
                    fill:  $color-white; 
                }
            }
        }
        .marquee-container {
            @extend .border-radius-3px;
            @extend .display-flex;
            overflow: hidden;
            padding: 15px 0px;
            margin: 0px 0px;
            width: 100%;
            
            .marquee {
                left: 100%;
                width: 100%;
                overflow: hidden;
                position: relative;
                white-space: nowrap;
                animation: marquee 15s linear infinite;
            }

            .marquee2 {
                animation-delay: 5s;
            }
            span { 
                @extend .color-white;
                font: -webkit-control;
                font-size: 15px;
            }
        }

        @keyframes marquee {
            0% {
                left: 100%;
            }
            100% {
                left: -100%
            }
        }
    }
</style>