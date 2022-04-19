<template>
    <div class="list-show">
        <div class="image-left">
            <amp-img alt="image" :src="firstImage" width="1" height="1" layout="responsive" />
        </div>
        <div class="image-right">
            <amp-img alt="image" :src="firstImage" width="1" height="1" layout="responsive" />
        </div>
    </div>
</template>

<script>
export default {
    props: {
        firstImage: String,
        secondImage: String,
    },
}
</script>

<style lang="scss">
     .list-show {
        @extend .display-grid;
        grid-template-columns: 1fr 1fr;
        margin: 10px 15px;
     }
</style>