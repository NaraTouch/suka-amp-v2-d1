<template>
    <div class="card-box">
        <div class="title">
            <title-image :customClass="customClassImageTitle" :customComponent="condition" :title="title" :width="width" :height="height" />
        </div>

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
    props : {
        title: String,
        linkButton: String,
        customClassImageTitle: String,
        customClassFirst: String,
        customClassSecond: String,
    },
    data() {
        return {
            width: "25",
            height: "30",
            condition: true,
        }
    },
}
</script>

<style lang="scss" amp-boilerplate>
    .card-box {
        background: $bg-body-field;
        @extend .border-radius-3px;
       
        .title {
            @extend .card-br-ig;
            border-top-right-radius: 3px;
            border-top-left-radius: 3px;
            padding: 3px 0px 3px 6px;
        }

        .footer-button {
            text-align: center;
            padding-bottom: 10px;
        }

        .btn-color {
            @extend .btn-custom;
            @extend .btn-bg-red;
            @extend .color-white;
        }
    }
</style>