<template>
    <div class="actions">
        <div></div>
        <div>
            <div class="display-list" v-for=" (image, index) in images" :key="index">
                <a class="connected-image" :href="image.url" target="_blank"><amp-img :src="image.src" width="50" height="45" :alt="image.alt"></amp-img></a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            images:[
                { src: "/images/footer/footer-home.png", url: "https://sukabet.com/", alt: "a sample image" },
                { src: "/images/footer/footer-profile.png", url: "https://sukabet.com/", alt: "a sample image" },
                { src: "/images/footer/footer-wallet.png", url: "https://sukabet.com/", alt: "a sample image" },
                { src: "/images/footer/footer-promo.png", url: "https://sukabet.com/", alt: "a sample image" },
                { src: "/images/footer/footer-chat.png", url: "https://sukabet.com/", alt: "a sample image" },
            ],
        }
    },
}
</script>

<style lang="scss">
    .actions {
        @extend .display-grid;
        @extend .z-index-1;
        position: fixed;
        bottom: -5px;
        grid-template-columns: 2.5fr 1fr;
        
        .display-list {
            @extend .display-inline-block;
            margin: 0px 10px 0px 0px;

            &:last-child {
                margin: 0px 0px 0px 0px;
            }
        }
    }
</style>