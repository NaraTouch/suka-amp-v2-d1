<template>
    <div class="card-box">
        <div class="title">
            <title-image :title="title" :image-title="imageTitle" :width="width" :height="height"/>
        </div>
        <div class="image-body">
            <ImageList :first-image="imageBodyFirst" :second-image="imageBodySecound" />
        </div>
        <div class="footer-button">
            <a :href="linkButton">
                <button class="btn btn-color">Lihat Semua</button>
            </a> 
        </div>
    </div>  
</template>

<script>
export default {
     components: {
        ImageList: () => import('../list/ImageList'),
        CustomButton: () => import('../button/CustomButton'),
        TitleImage: () => import('../TitleImage'),
    },
    props : {
        title: String,
        imageTitle: String,
        imageBodyFirst: String,
        imageBodySecound: String,
        linkButton: String,
    },
    data() {
        return {
            images: "/images/card/poker-thumb.png",
            width: "25",
            height: "30",
        }
    },
}
</script>

<style lang="scss">
    .card-box {
        background: $bg-body-field;
        border-radius: 3px;
       
        .title {
            @extend .card-br-ig;
             border-top-right-radius: 3px;
            border-top-left-radius: 3px;
            padding: 3px 0px 3px 10px;
        }

        .footer-button {
            text-align: center;
            padding-bottom: 10px;
        }

        .btn {
            border: 1px;
            padding: 8px 40px 8px 40px;
            border-radius: 3px;
            font-weight: 600;
        }
        
        .btn-color {
            @extend .btn-bg-red;
            color: $color-white;
        }
    }
</style>