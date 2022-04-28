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
                <content-text />
            </div>
        </section>

        <article class="column-right">
            
            <!-- body-container-sport -->
            <div class="body-container-sport">
                <title-image :hrContainerTitle="hrContainerTitle" :CustomClassStyle="customClassStyle" :customClass="classStyle" :customComponent="condition" :title="title" :width="width" :height="height" />
            </div>
            
            <!-- card-content -->
            <div class="card-content-sport">
                <card-game :cardMultiple="cardMultiple" :CardDataOneSlots="CardDataOneSlots" :customimageClassStyle="customimageClassStyle" :oneimageBodyCustom="oneimageBodyCustom" />
            </div>
        </article>
    </div>
</template>

<script>
    export default {
        components: {
            TabWinner: () => import('../Tab/TabWinner'),
                Slider: () => import('../slider/Slider'),
        },
         data() {
            return {
                cardMultiple: false,
                count: 0,
                src: "../static/images/images.jpg",
                sliderPromotion: "/data/slider-list.json",
                sliderImage: "/data/slider-image-list.json",
                slderCondition: true, 
                width: "25",
                height: "30",
                condition: true,
                title: "CASINO",
                classStyle: "item-custom-casino",
                customClassStyle: true,
                hrContainerTitle: "hr-conatiner-title",

                CardDataOneSlots: [
                    {
                        bgGame: { 
                            multipleImage: false,
                            cardTitle: false,
                            title: "DG",
                            classStyle: "maxbet-image",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-casino",
                            oneimageBodyCustom: "oneimage-body-custom",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                        },
                        idnGame: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "IDNGAME",
                            classStyle: "co9-sport-image",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-casino",
                            oneimageBodyCustom: "oneimage-body-custom",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                        },
                        C09Live: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "C09LIVE",
                            classStyle: "cmd-368-image",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-casino",
                            oneimageBodyCustom: "oneimage-body-custom",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                        },
                        HoGaming: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "HOGAMING",
                            classStyle: "ho-gaming",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-casino",
                            oneimageBodyCustom: "oneimage-body-custom",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                        },
                        DreamGaming: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "DREAM GAMING",
                            classStyle: "pragmatic-play",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-casino",
                            oneimageBodyCustom: "oneimage-body-custom",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                        },
                        D88GreenDragon: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "D88 GREEN DRAGON",
                            classStyle: "green-dragon",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-casino",
                            oneimageBodyCustom: "oneimage-body-custom",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                        },
                        WWCasino: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "WW CASINO",
                            classStyle: "ww-casino",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-casino",
                            oneimageBodyCustom: "oneimage-body-custom",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                        },
                        ICONCasino: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "ICON CASINO",
                            classStyle: "icon-casino",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-casino",
                            oneimageBodyCustom: "oneimage-body-custom",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
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
                @extend .mr-box;
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
            
            .body-container-sport {
                @extend .btn-bg-red;
                @extend .border-radius-3px;
                // padding: 10px 0px;
            }

            .card-content-sport {
                border-bottom: 1px solid $border-right-cr;
                padding-bottom: 10px;
            }

            // .slider-image {
            //     background-color: $bg-body-field;
            // }

            // .card-content {
            //     padding: 10px 0px 0px 0px;
            // }
        }
    }
</style>