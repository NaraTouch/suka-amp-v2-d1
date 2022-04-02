<template>
    <div>
            <amp-carousel id="carouselWithPreview" width="400" height="300" layout="responsive" type="slides" on="slideChange:carouselWithPreviewSelector.toggle(index=event.index, value=true)">
            <amp-img src="https://unsplash.it/400/300?image=10" layout="fill" alt="a sample image"></amp-img>
            <amp-img src="https://unsplash.it/400/300?image=11" layout="fill" alt="a sample image"></amp-img>
            <amp-img src="https://unsplash.it/400/300?image=12" layout="fill" alt="a sample image"></amp-img>
            <amp-img src="https://unsplash.it/400/300?image=13" layout="fill" alt="a sample image"></amp-img>
        </amp-carousel>
  </div>
</template>

<script>
export default {
    
}
</script>
<style lang="scss">
    
</style>