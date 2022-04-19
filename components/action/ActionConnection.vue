<template>
    <div class="action">
        <div class="left-div"></div>
        <div class="right-div">
            <amp-list class="display-list" width="auto" height="70" layout="fixed-height" src="/data/action-list.json" v-html="actionList" />
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            actionList: `
                <template type="amp-mustache">
                    <amp-carousel  class="connected-image" id="custom-button"  width="50" height="50" type="slides" >
                        <a class="image-pd" href="{{link}}" target="_blank"> <amp-img src="{{image}}" width="50" height="50" layout="responsive" alt="AMP Carousel"></amp-img></a>
                    </amp-carousel>
                </template>
            `
        }
    },
}
</script>
<style lang="scss">
    .action {
        @extend .position-fixed;
        z-index: 9999;
        bottom: -240px;

        // set 2 path to move button to right equal to card 
        @extend .display-grid;
        grid-template-columns: 2.54fr 1fr;

        .right-div {
            .display-list {
                padding: 145px;
                .connected-image {
                    margin: 0px 10px 0px 0px;
                    &:last-child {
                        margin: 0px 0px 0px 0px;
                    }
                }
            } 
        }
    }
</style>