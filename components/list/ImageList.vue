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
    data() {
        return {
          
        }
    },
}
</script>

<style lang="scss">
     .list-show {
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-gap: 10px;
        margin: 10px 20px;
     }
</style>