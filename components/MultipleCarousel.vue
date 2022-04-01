<template>
    <div class="margin-slide">
        <amp-carousel  class="padding" height="150" layout="fixed-height" type="carousel" role="region" aria-label="Basic usage carousel">
            <div v-for=" (ampImage, index) in ampImages" :key="index">
                <div class="image-size">
                    <amp-img sizes="(max-width: 767px) 100px, 150px" class="image-space" :src="ampImage.src" :width="ampImage.width" :height="ampImage.height" :alt="ampImage.alt"></amp-img>
                </div>
            </div>
        </amp-carousel>
    </div>
</template>

<script>
export default {
   data() {
       return {
           ampImages: [
               { src: "https://amp.dev/static/samples/img/image1.jpg", width: "150", height: "150", alt: "a sample image", },
               { src: "https://amp.dev/static/samples/img/image2.jpg", width: "150", height: "150", alt: "a sample image", },
               { src: "https://amp.dev/static/samples/img/image3.jpg", width: "150", height: "150", alt: "a sample image", },
               { src: "https://amp.dev/static/samples/img/image1.jpg", width: "150", height: "150", alt: "a sample image", },
               { src: "https://amp.dev/static/samples/img/image2.jpg", width: "150", height: "150", alt: "a sample image", },
               { src: "https://amp.dev/static/samples/img/image3.jpg", width: "150", height: "150", alt: "a sample image", },
               { src: "https://amp.dev/static/samples/img/image2.jpg", width: "150", height: "150", alt: "a sample image", },
               { src: "https://amp.dev/static/samples/img/image3.jpg", width: "150", height: "150", alt: "a sample image", },
               { src: "https://amp.dev/static/samples/img/image1.jpg", width: "150", height: "150", alt: "a sample image", },
           ],
       }
   },
}
</script>

<style lang="scss" scoped>
    .margin-slide {
        margin: 10px -13px;
        .padding {
            padding: 0px 100px;
            @media #{$xl-device} {
                    padding: 0px 60px;
            }
            .image-space {
                margin: 0px 15px;
                border-radius: 20px;
                border: 1px solid $border-color-1;
               @media #{$xl-device} {
                    margin: 0px 10px;
               }
            }
        }  
    }
   @media #{$sm-device} {
        .margin-slide {
            .padding {
                .image-space amp-img {
                       
                }
            }
        }
    } 
    // @media #{$xl-device} {
    //     .padding {
    //         padding: 0px 60px;
    //          .image-space {
    //             margin: 0px 10px;
    //          }
    //     }
    // }
  
</style>