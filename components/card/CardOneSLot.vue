<template>
    <div class="card-box">
        <div class="image-body">
            <ImageList :customClassSecond="customClassSecond" :customClassFirst="customClassFirst" />
        </div>
        
        <div class="footer-button">
            <a :href="linkButton">
                <button class="btn-color">Lihat Semua</button>
            </a> 
        </div>
    </div>  
</template>

<script>
export default {
    components: {
        ImageList: () => import('../list/ImageList'),
        TitleImage: () => import('../TitleImage'),
    },
}
</script>

<style lang="scss">
    
</style>