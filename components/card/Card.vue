<template>
    <div class="card-box">
        <div class="title">
            <h2>hello world</h2>
        </div>
        <div class="image-body">
            <ImageList />
        </div>
        <div class="footer-button">
            <CustomButton />
        </div>
    </div>
</template>

<script>
export default {
     components: {
        ImageList: () => import('../list/ImageList'),
        CustomButton: () => import('../button/CustomButton')
    },
    data() {
        return {
            images: "/images/card/poker-thumb.png",
        }
    },
}
</script>

<style lang="scss">
    .card-box {
        background: $color-gray;
        .title {
            background: $color-gray;
            padding: 10px 0px 0px 15px;
            text-align: justify;
        }
        .footer-button {
            padding: 0px 0px 10px 0px;
        }
    }
</style>