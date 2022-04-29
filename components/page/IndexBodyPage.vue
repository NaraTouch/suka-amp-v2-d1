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
                <card-game :cardMultiple="cardMultiple" />
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

            .slider-image {
                background-color: $bg-body-field;
            }

            .card-content {
                padding: 10px 0px 0px 0px;
            }
        }
    }
</style>