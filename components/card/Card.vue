<template>
    <div class="card-box">
        <div v-if="cardTitle" class="title">
            <title-image :CustomClassStyle="customClassStyle" :customClass="customClassImageTitle" :customComponent="condition" :title="title" :width="width" :height="height" />
        </div>

        <div v-if="multipleImage" class="image-body">
            <image-list :customClassSecond="customClassSecond" :customClassFirst="customClassFirst" />
        </div>

        <div class="oneimage-body" v-else>
            <image-one :customClass="customClassImageOne" /> 
        </div>
        
        <div class="footer-button">
            <a :href="linkButton">
                <button class="btn-color" :class="btnStyle"> {{ btnTitle }}</button>
            </a> 
        </div>
    </div>  
</template>

<script>
    export default {
        components: {
            ImageList: () => import('../list/ImageList'),
            TitleImage: () => import('../TitleImage'),
            ImageOne: () => import('../list/ImageOne'),
        },
        props : {
            cardTitle: Boolean,
            title: String,
            linkButton: String,
            multipleImage: Boolean,
            customClassImageTitle: String,
            customClassFirst: String,
            customClassSecond: String,
            customClassImageOne: String,
            btnTitle: String,
            btnStyle: String,
        },  
        data() {
            return {
                width: "25",
                height: "30",
                condition: true,
                customClassStyle: false,
                spanStyle: "span-style",
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

            .btn-style {
                padding: 7px 25px 7px 25px; 
            }
        }

        .btn-color {
            @extend .btn-custom;
            @extend .btn-bg-red;
            @extend .color-white;
        }

        .oneimage-body {
            padding: 10px;
        }
    }
</style>