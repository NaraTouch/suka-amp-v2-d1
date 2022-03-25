<template>
     <div class="image-size">
        <amp-img :src="src" :width="width" :height="height" alt="a non-existent image"></amp-img>
    </div>
</template>

<script>
export default {
    props: {
        src: String,
        width: String,
        height: String,
    }
}
</script>

<style lang="scss" scoped>
    .image-size {
        height: 20px;
    }
</style>

