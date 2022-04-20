<template>
    <div class="inner-grid">
        <div class="bg-color-ig" v-for=" (ampImage, index) in ampImages" :key="index">
            <NuxtLink :to="ampImage.url" class="header-logo">
                <amp-img class="test" :src="ampImage.src" width="1" height="1" layout="responsive" alt="AMP Carousel"></amp-img>
            </NuxtLink>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            ampImages:[
               { src: "/images/navbar-logo/01-hot-games.png", url:"/", alt: "a sample image", },
               { src: "/images/navbar-logo/02-sports.png", url:"/", alt: "a sample image" },
               { src: "/images/navbar-logo/03-casino.png", url:"/", alt: "a sample image" },
               { src: "/images/navbar-logo/04-slots.png", url:"/", alt: "a sample image" },
               { src: "/images/navbar-logo/05-poker.png", url:"/", alt: "a sample image" },
               { src: "/images/navbar-logo/06-togel.png", url:"/", alt: "a sample image" },
               { src: "/images/navbar-logo/07-arcade.png", url:"/", alt: "a sample image" },
               { src: "/images/navbar-logo/08-cock-fight.png", url:"/", alt: "a sample image" },
               { src: "/images/navbar-logo/09-lucky-spin.png", url:"/", alt: "a sample image" }
            ],
        }
    },
}
</script>

<style lang="scss" scoped>
    .inner-grid {
        @extend .display-grid;
        grid-template-columns: repeat(9, 1fr);
        grid-auto-rows: 100px;
        grid-column-gap: 10px;

        .bg-color-ig {
            @extend .nav-image-bg;
            @extend .border-radius-3px;
            height: max-content;
            &:last-child {
                @extend .free-daily-spain;
            }
        }
    }
</style>