<template>
    <div >
        <amp-list class="slider" height="300" items="." single-item="." src= "/data/slider-list.json" v-html="listSlier" /> 
    </div>
</template>

<script>
export default {
    data() {
        return {
            listSlier: `
                <template type="amp-mustache">
                    <amp-carousel width="239" height="400" class="carousel" type="slides" autoplay lightbox delay="3000">
                            {{#items}}
                            <div class="slide">           
                                <amp-img src="{{url}}"
                                width="239" height="400"
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
    .carousel {
        .slide > amp-img > img {
            object-fit: contain;
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
            max-height: 30%;
        }
    }
</style>