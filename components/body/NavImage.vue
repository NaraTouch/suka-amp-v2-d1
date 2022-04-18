<template>
    <div class="inner-grid">
        <div class="bg-color-ig" v-for=" (ampImage, index) in ampImages" :key="index">
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

        .bg-color-ig {
            @extend .nav-image-bg;
            background-repeat: repeat-x;
            background-size: contain;
            height: max-content;
            border-radius: 5px;
        }
    }
</style>