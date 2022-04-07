<template>
    <div>
        <div v-if="slider" class="slider-promotion">
            <!-- <amp-list class="slider" width="375" height="400" items="." single-item="." :src="slideList" v-html="listSlierPromotion" />  -->
            <amp-img class="image-br" :src="imagePromotion" height="360" layout="fixed-height"></amp-img>
        </div>
        <div v-else class="test">
            <amp-list class="slider" height="280" items="." single-item="." layout="fixed-height" :src= "slideList" v-html="listSlierImage" />
        </div>
    </div>
</template>

<script>
export default {
    props: {
        slideList: String,
        slider: Boolean,
    },
    data() {
        return {
            imagePromotion: '/images/slider-promotion/Sidebar-Banner.png',
            listSlierPromotion: `
                <template type="amp-mustache">
                    <amp-carousel class="carousel" width="375" height="400"  type="slides" autoplay lightbox delay="3000">
                            {{#items}}
                            <div class="slide">           
                                <amp-img src="{{url}}"
                                width="375" height="400"
                                layout="responsive"></amp-img>
                            </div>
                        {{/items}}
                    </amp-carousel>
                </template>
            `,
            listSlierImage: `
                <template type="amp-mustache">
                    <amp-carousel  height="280" class="carousel" layout="fixed-height" type="slides" autoplay lightbox delay="3000">
                            {{#items}}
                            <div class="slide">           
                                <amp-img src="{{url}}"
                                 layout="fixed-height" height="280"
                                ></amp-img>
                            </div>
                        {{/items}}
                    </amp-carousel>
                </template>
            `
        }
    },
}
</script>

<style lang="scss">
    .slider-promotion {
        .image-br {
            @extend .border-radius-5px;
        }
        .carousel {
            border-radius: 10px;
            .slide > amp-img > img {
                // position: fixed;
            }
            // .caption {
            //     position: absolute;
            //     bottom: 0;
            //     left: 0;
            //     right: 0;
            //     padding: .5rem;
            //     background: rgba(0, 0, 0, 0.6);
            //     font-family:Arial;
            //     color: white;
            //     max-height: 20%;
            // }
        }
    }
    .test {
        margin: 0px 0px -2px;
        .slider {
             @extend .card;
        }
        .carousel {
            .slide > amp-img > img {
                // object-fit: contain;
                //  position: fixed;
            }
            // .caption {
            //     position: absolute;
            //     bottom: 0;
            //     left: 0;
            //     right: 0;
            //     // padding: .5rem;
            //     background: rgba(0, 0, 0, 0.6);
            //     font-family:Arial;
            //     color: white;
            //     max-height: 20%;
            // }
        }
    }
</style>