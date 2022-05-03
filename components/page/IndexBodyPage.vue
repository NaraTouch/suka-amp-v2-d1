<template>
    <div class="body-field">
        <section class="column-left">
            <!-- tab-winner -->
            <div class="tab-winner">
                <tab-winner />
            </div>

            <div class="border-row">
                <!-- slider-promotion -->
                <div class="slider-promotion">
                    <slider :slide-list="sliderPromotion" :slider="slderCondition" />
                </div>
                <!-- stay-connected -->
                <div class="stay-connected">
                    <stay-connected />
                </div>

                <!-- payment-method -->
                <div class="payment-method">
                    <payment-method />
                </div>
            </div>

            <!-- contect-text -->
            <div class="content-text">
                <content-text :width="widthContentText" :height="heightContentText" :ContentText="ContentText" />
            </div>
        </section>

        <article class="column-right">
            <!-- slider-image -->
            <div class="slider-image">
                <slider :slide-list="sliderImage" />
                <slider-path />
            </div>

            <div class="card-content">
                <card-game :cardMultiple="cardMultiple" :cardDatas="cardDatas" />
            </div>
        </article>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                widthContentText: "243px",
                heightContentText: "105px",
                ContentText: 'Selamat datang di situs Sukabet, situs permainan online terlengkap dan terpercaya. Pada halaman ini anda dapat memilih kategori permainan yang anda ingin mainkan saat ini. Bagi anda yang belum memiliki akun, silahkan membuat akun dengun mengklik "Datfar" dan',
                cardMultiple: true,
                sliderPromotion: "/data/slider-list.json",
                sliderImage: "/data/slider-image-list.json",
                slderCondition: true, 
                cardDatas: [
                    { 
                        hotGames: {
                            multipleImage: true,
                            cardTitle: true,
                            title: "Hot Games",
                            link: "https://www.w3schools.com/",
                            customClassFirst: "item-custom-hot-game-first",
                            customClassSecond: "item-custom-hot-game-second",
                            classStyle: "item-custom-hot-game",
                            btnTitle: "Lihat Semua",
                            buttonClick: true
                        },
                        sportsGames: {
                            multipleImage: true,
                            cardTitle: true,
                            title: "Sports",
                            link: "https://www.w3schools.com/",
                            customClassFirst: "item-custom-sports-first",
                            customClassSecond: "item-custom-sports-second",
                            classStyle: "item-custom-sports",
                            btnTitle: "Lihat Semua",
                            buttonClick: true
                        },
                        casinoGames: {
                            multipleImage: true,
                            cardTitle: true,
                            title: "Casino",
                            link: "https://www.w3schools.com/",
                            customClassFirst: "item-custom-casino-first",
                            customClassSecond: "item-custom-casino-second",
                            classStyle: "item-custom-casino",
                            btnTitle: "Lihat Semua",
                            buttonClick: true
                        },
                        slotsGames: {
                            multipleImage: true,
                            cardTitle: true,
                            title: "Slots",
                            link: "https://www.w3schools.com/",
                            customClassFirst: "item-custom-slots-first",
                            customClassSecond: "item-custom-slots-second",
                            classStyle: "item-custom-slots",
                            btnTitle: "Lihat Semua",
                            buttonClick: true
                        },
                        pokerGames: {
                            multipleImage: true,
                            cardTitle: true,
                            title: "Poker",
                            link: "https://www.w3schools.com/",
                            customClassFirst: "item-custom-poker-first",
                            customClassSecond: "item-custom-poker-second",
                            classStyle: "item-custom-poker",
                            btnTitle: "Lihat Semua",
                            buttonClick: true
                        },
                        arcadeGames: {
                            multipleImage: true,
                            cardTitle: true,
                            title: "Arcade",
                            link: "https://www.w3schools.com/",
                            customClassFirst: "item-custom-arcade-first",
                            customClassSecond: "item-custom-arcade-second",
                            classStyle: "item-custom-arcade",
                            btnTitle: "Lihat Semua",
                            buttonClick: true
                        },
                        TogelGames: {
                            multipleImage: true,
                            cardTitle: true,
                            title: "Togel",
                            link: "https://www.w3schools.com/",
                            customClassFirst: "item-custom-togel-first",
                            customClassSecond: "item-custom-togel-second",
                            classStyle: "item-custom-togel",
                            btnTitle: "Lihat Semua",
                            buttonClick: true
                        },
                        cockFightingGames: {
                            multipleImage: true,
                            cardTitle: true,
                            title: "Cock Fighting",
                            link: "https://www.w3schools.com/",
                            customClassFirst: "item-custom-cock-fighting-first",
                            customClassSecond: "item-custom-cock-fighting-second",
                            classStyle: "item-custom-cock-fighting",
                            btnTitle: "Lihat Semua",
                            buttonClick: true
                        },
                    }
                ],
            };
        },
    }
</script>

<style lang="scss" amp-boilerplate>
    .body-field {
        @extend .display-flex;
        margin: 10px 0px 30px 0px;

        .border-row {
            @extend .z-index-1;
            padding: 0px 13px 0px 0px;
            margin: 0px -16px 0px 0px;
            position: relative;

            &:before {
                @extend .border-right;
                content: "";
                position: absolute;
                bottom: 112px;
                right: 0;
                height: 87%;
            }
        }

        .column-left {
            min-width: 265px;
            padding-right: 15px;

            .tab-winner {
                border-bottom-right-radius: 4px;
            }

            .slider-promotion {
                margin: 10px 0px;
            }

            .stay-connected {
                margin-bottom: 30px;
                background-color: $bg-body-field;
                @extend .border-radius-3px;
            }

            .payment-method {
                padding-bottom: 15px;
                @extend .border-radius-3px;
                background-color: $bg-body-field;
            }

            .content-text {
                margin-top: 20px;
            }
        }

        .column-right {
            min-width: 760px;
            padding-left: 15px;

            .slider-image {
                background-color: $bg-body-field;
            }

            .card-content {
                padding: 10px 0px 0px 0px;
            }
        }
    }
</style>