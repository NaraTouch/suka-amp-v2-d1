<template>
    <div class="header-title">
        <div class="image">
            <amp-img alt="image" :src="imageTitle" :width="width" :height="height" />
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
        width: String, 
        height: String,
     }
}
</script>

<style lang="scss">
    .header-title {
        @extend .display-flex;
       
        .title-card {
            padding: 7px 0px 0px 10px;
            color: $text-color-1;
        }
    }
</style>