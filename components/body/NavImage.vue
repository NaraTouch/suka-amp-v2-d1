<template>
    <div class="image">
        <div class="image-size"  v-for=" (ampImage, index) in ampImages" :key="index">
            <amp-img sizes="(max-width: 767px) 100px, 140px" class="image-space" :src="ampImage.src" :width="ampImage.width" :height="ampImage.height" :alt="ampImage.alt"></amp-img>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            ampImages: [
               { src: "https://amp.dev/static/samples/img/image1.jpg", width: "130", height: "130", alt: "a sample image", },
               { src: "https://amp.dev/static/samples/img/image2.jpg", width: "130", height: "130", alt: "a sample image", },
               { src: "https://amp.dev/static/samples/img/image3.jpg", width: "130", height: "130", alt: "a sample image", },
               { src: "https://amp.dev/static/samples/img/image1.jpg", width: "130", height: "130", alt: "a sample image", },
               { src: "https://amp.dev/static/samples/img/image2.jpg", width: "130", height: "130", alt: "a sample image", },
               { src: "https://amp.dev/static/samples/img/image3.jpg", width: "130", height: "130", alt: "a sample image", },
               { src: "https://amp.dev/static/samples/img/image2.jpg", width: "130", height: "130", alt: "a sample image", },
               { src: "https://amp.dev/static/samples/img/image3.jpg", width: "130", height: "130", alt: "a sample image", },
               { src: "https://amp.dev/static/samples/img/image1.jpg", width: "130", height: "130", alt: "a sample image", },
           ],
        }
    },
}
</script>

<style lang="scss" scoped>
    .image {
        margin-bottom: 10px;
        .image-size {
            display: inline-block;
            margin: 0px 28px 0px 0px;
            &:last-child {
                margin: 0px 0px 0px 0px;
            }
            .image-space {
                border-radius: 5px;
                border: 1px solid $color-white;
            }
        }
    }
</style>