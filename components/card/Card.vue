<template>
    <div class="card-box">
        <div v-if="cardTitle" class="title">
            <title-image :CustomClassStyle="customClassStyle" :customClass="customClassImageTitle" :customComponent="condition" :title="title" :width="width" :height="height" />
        </div>

        <div v-if="multipleImage" class="image-body">
            <image-list :customClassSecond="customClassSecond" :customClassFirst="customClassFirst" />
        </div>

        <div v-else class="oneimage-body" :class="oneimageBodyCustom">
            <image-one :customClass="customClassImageOne" :customimageClassStyle="customimageClassStyle" /> 
        </div>
        
        <div v-if="buttonClick" class="footer-button">
            <a :href="linkButton">
                <button class="btn-color" :class="btnStyle"> {{ btnTitle }}</button>
            </a> 
        </div>

        <div class="loading-style" v-if="loadingClick">
            <a >
                <button class="btn-loading-style" >
                   <loading-style />
                </button>
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
            LoadingStyle: () => import('../slotGame/LoadingStyle')
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
            customimageClassStyle: String,
            oneimageBodyCustom: String,
            btnStyle: String,
            buttonClick: Boolean,
            loadingClick: Boolean,
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
            cursor: pointer;
        }

        .oneimage-body {
            padding: 10px;
        }
        .oneimage-body-custom {
            padding: 10px 0px;
        }
        .loading-style {
            a {
               .btn-loading-style {
                    cursor: pointer;
               }
            }
        }
    }
</style>