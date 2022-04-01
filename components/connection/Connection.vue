<template>
    <div class="connection-list">
        <span> Stay connected </span>
        <amp-list class="connection" width="auto" height="70" layout="fixed-height" src="/data/connection-list.json" v-html="imageList" />
    </div>
</template>

<script>
export default {
    data() {
        return {
            imageList: `
                <template type="amp-mustache">
                    <amp-carousel id="custom-button"  width="50" height="50" type="slides" >
                        <a href="{{logo}}" target="_blank"> <amp-img src="{{logo}}" width="50" height="50" layout="responsive" alt="AMP Carousel"></amp-img></a>
                    </amp-carousel>
                </template>
            `
        }
    },
}
</script>

<style lang="scss">
    .connection-list {
        margin: 15px 0px 0px 0px;
        span {
            display: flex;
            margin: 0px 0px 0px 20px;
        }
        .list-overflow[overflow] {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            }
            .connection {
                margin: 10px 0px 0px 0px;
            }
    }
</style>