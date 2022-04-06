<template>
    <div class="list-show">
        <amp-list class="image-list" height="230" layout="fixed-height" src="/data/card/list-image.json" v-html="imageList" />
        <!-- <amp-img sizes="(max-width: 767px) 100px, 140px" class="image-space" :src="ampImage.src" :width="ampImage.width" :height="ampImage.height" :alt="ampImage.alt"></amp-img> -->
        <!-- <amp-img lightbox :src="image" layout="fixed" width="400" height="400" /> -->
    </div>
</template>

<script>
export default {
    props: {
        image: String,
    },
    data() {
        return {
            imageList: `
                <template type="amp-mustache">
                    <amp-carousel  class="connected-image" id="custom-button"  width="200" height="200" type="slides">
                       <amp-img class="test" src="{{image}}" width="200" height="200" layout="responsive" alt="AMP Carousel"></amp-img>
                    </amp-carousel>
                </template>
            `
        }
    },
}
</script>

<style lang="scss">
     .list-show {
        .image-list {
            display: flex;
            .connected-image {
                margin: 10px;
                &:first-child {
                    margin-right: 40px;
                }
                .test {
                   
                }
            }
        }
     }
</style>