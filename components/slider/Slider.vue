<template>
    <div>
        <div v-if="slider" class="slider-promotion">
            <amp-list class="slider" height="400" items="." single-item="." :src="slideList" v-html="listSlierPromotion" /> 
        </div>
        <div v-else class="slider-image">
            <amp-list class="slider" height="300" items="." single-item="." :src= "slideList" v-html="listSlierImage" />
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
            listSlierPromotion: `
                <template type="amp-mustache">
                    <amp-carousel class="carousel" width="239" height="400"  type="slides" autoplay lightbox delay="3000">
                            {{#items}}
                            <div class="slide">           
                                <amp-img src="{{url}}"
                                width="239" height="400"
                                layout="responsive"></amp-img>
                            </div>
                        {{/items}}
                    </amp-carousel>
                </template>
            `,
            listSlierImage: `
                <template type="amp-mustache">
                    <amp-carousel width="700" height="300" class="carousel" type="slides" autoplay lightbox delay="3000">
                            {{#items}}
                            <div class="slide">           
                                <amp-img src="{{url}}"
                                width="700" height="300"
                                layout="responsive"></amp-img>
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
        .carousel {
            .slide > amp-img > img {
                // object-fit: contain;
            }
            .caption {
                position: absolute;
                bottom: 0;
                left: 0;
                right: 0;
                padding: .5rem;
                background: rgba(0, 0, 0, 0.6);
                font-family:Arial;
                color: white;
                max-height: 20%;
            }
        }
    }
    .slider-image {
        .slider {
            @extend .card;
        }
        .carousel {
            .slide > amp-img > img {
                // object-fit: contain;
            }
            .caption {
                position: absolute;
                bottom: 0;
                left: 0;
                right: 0;
                padding: .5rem;
                background: rgba(0, 0, 0, 0.6);
                font-family:Arial;
                color: white;
                max-height: 20%;
            }
        }
    }
</style>