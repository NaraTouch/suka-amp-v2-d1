<template>
    <div class="inner-grid">
        <!-- <div class="image">
            <div class="image-size"  v-for=" (ampImage, index) in ampImages" :key="index">
                <amp-img sizes="(max-width: 767px) 100px, 140px" class="image-space" :src="ampImage.src" :width="ampImage.width" :height="ampImage.height" :alt="ampImage.alt"></amp-img>
            </div>
        </div> -->
            <div v-for=" (ampImage, index) in ampImages" :key="index">
                <a :href="ampImage.url" target="_blank"> 
                    <amp-img :src="ampImage.src" width="1" height="1" layout="responsive" alt="AMP Carousel"></amp-img>
                </a>
            </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            ampImages:[
               { src: "/images/navbar-logo/01-hot-games.png", url:"https://www.w3schools.com/css/css_grid.asp", alt: "a sample image", },
               { src: "/images/navbar-logo/02-sports.png", url:"https://www.w3schools.com/css/css_grid.asp", alt: "a sample image" },
               { src: "/images/navbar-logo/03-casino.png", url:"https://www.w3schools.com/css/css_grid.asp", alt: "a sample image" },
               { src: "/images/navbar-logo/04-slots.png", url:"https://www.w3schools.com/css/css_grid.asp", alt: "a sample image" },
               { src: "/images/navbar-logo/05-poker.png", url:"https://www.w3schools.com/css/css_grid.asp", alt: "a sample image" },
               { src: "/images/navbar-logo/06-togel.png", url:"https://www.w3schools.com/css/css_grid.asp", alt: "a sample image" },
               { src: "/images/navbar-logo/07-arcade.png", url:"https://www.w3schools.com/css/css_grid.asp", alt: "a sample image" },
               { src: "/images/navbar-logo/08-cock-fight.png", url:"https://www.w3schools.com/css/css_grid.asp", alt: "a sample image" },
               { src: "/images/navbar-logo/09-lucky-spin.png", url:"https://www.w3schools.com/css/css_grid.asp", alt: "a sample image" }
            ]
        }
    },
}
</script>

<style lang="scss" scoped>
    .inner-grid {
        display: grid;
        grid-template-columns: repeat(9, 1fr);
        grid-auto-rows: 100px;
        
        grid-column-gap: 10px;
        div {
            
        }
         // Mobile Landscpe
        @media #{$md-device} { 
            
        }

        // mobile 
        @media #{$sm-device} { 

        }
        // .image {
        //     margin-bottom: 10px;
        //     .image-size {
        //         display: inline-block;
        //         margin: 0px 28px 0px 0px;
        //         &:last-child {
        //             margin: 0px 0px 0px 0px;
        //         }
        //         .image-space {
        //             border-radius: 5px;
        //             border: 1px solid $color-white;
        //         }
        //     }
        // }
    }
</style>