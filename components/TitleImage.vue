<template>
    <div class="header-title">
        <div class="image">
            <amp-img alt="image" :src="imageTitle" width="25" height="30" />
        </div>
        <div class="title-card">
            <span class="span-right">{{title}}</span>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        title: String,
        imageTitle: String,
     }
}
</script>

<style lang="scss">
    .header-title {
        display: flex;
        .image {

        }
        .title-card {
            padding: 7px 0px 0px 10px;
            color: $text-color-1;
        }
    }
</style>