<template>
    <div>
        <div v-if="slider" class="slider-promotion">
            <amp-img class="image-br" :src="imagePromotion" height="400" layout="fixed-height"></amp-img>
        </div>
        <div v-else class="list-slider">
            <amp-list class="slider" height="280" items="." single-item="." layout="fixed-height" :src= "slideList" v-html="listSliderImage" />
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
            listSliderImage: `
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

<style lang="scss" amp-boilerplate>
    .slider-promotion {
        .image-br {
            @extend .border-radius-3px;
        }
    }
    .list-slider {
        margin: 0px 0px -2px;
        .slider {
             @extend .card;
        }
    }
</style>