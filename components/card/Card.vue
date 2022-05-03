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
       
        .test {
             #modalbox {
      z-index: 10000
    }

    // .modalbox {
    //   display: flex;
    //   align-items: center;
    //   justify-content: center;
    //   z-index: 1;
    //   background: rgba(0, 0, 0, 0.5);
    //   width: 100%;
    //   height: 100%;
    //   position: fixed;
    // }

    // .modal_box {
    //   margin-left: -25%;
    //   z-index: 99;
    //   border-radius: 4px;
    //   box-shadow: 0 9px 46px 8px rgba(0, 0, 0, .14), 0 11px 15px -7px rgba(0, 0, 0, .12), 0 24px 38px 3px rgba(0, 0, 0, .2);
    //   font-family: Roboto, sans-serif;
    //   position: absolute;
    //   padding: 3px;
    //   top: 15%;
    //   transition: all .3s ease-in-out;
    //   width: 50%;
    //   left: 50%;
    //   background-image: linear-gradient(45deg, #fae900 25%, #383838 25%, #383838 50%, #fae900 50%, #fae900 75%, #383838 75%, #383838 100%);
    //   background-size: 40px 40px;
    // }

    // .modal_box .warn {
    //   border-radius: 4px;
    //   background: #fff;
    //   color: #555;
    //   padding: 15px;
    // }

    // .modal_box p {
    //   font-weight: 400;
    //   line-height: 1.3;
    //   margin: 0;
    //   padding: 0;
    //   font-size: 14px;
    // }

    // .modal_box h4 {
    //   margin: 0 0 10px;
    //   line-height: 1;
    //   color: #333;
    //   font-size: 18px;
    //   font-weight: 500;
    // }

    // hr {
    //   height: 0;
    //   border: 0;
    //   border-top: 1px solid #eee;
    // }

    // .modalbox .close_modalbox {
    //   line-height: 20px;
    //   text-align: center;
    //   padding: 0;
    //   color: #555;
    //   font-size: 30px;
    //   position: absolute;
    //   top: 23px;
    //   background: 0 0;
    //   border: none;
    //   right: 23px;
    //   cursor: pointer;
    //   width: 20px;
    //   height: 20px;
    // }

    // .modalbox .close_modalbox:focus,
    // .modalbox .done_modalbox:focus {
    //   outline: none
    // }

    // .modalbox .done_modalbox {
    //   padding: 10px 13px;
    //   border-radius: 3px;
    //   box-shadow: 0 2px 2px 0 rgba(0, 0, 0, .14), 0 3px 1px -2px rgba(0, 0, 0, .2), 0 1px 5px 0 rgba(0, 0, 0, .12);
    //   background: #009688;
    //   color: #fff;
    //   border: none;
    //   margin-top: 15px;
      
    //   font-family: Roboto, sans-serif;
    //   font-size: 14px;
    //   font-weight: 500;
    //   text-transform: uppercase;
    //   cursor: pointer
    // }

    // .modalbox .close_modalbox:hover {
    //   color: #C51162
    // }

    // .modalbox .done_modalbox:hover {
    //   background: #008688
    // }
    // .txt-r{text-align:right}
    // .slideInDown {
    //   -webkit-animation-name: slideInDown;
    //   animation-name: slideInDown;
    //   -webkit-animation-duration: .4s;
    //   animation-duration: .4s;
    //   -webkit-animation-fill-mode: both;
    //   animation-fill-mode: both
    // }

    // @-webkit-keyframes slideInDown {
    //   0% {
    //     -webkit-transform: translateY(-100%);
    //     transform: translateY(-100%);
    //     visibility: visible
    //   }
    //   100% {
    //     -webkit-transform: translateY(0);
    //     transform: translateY(0)
    //   }
    // }

    // @keyframes slideInDown {
    //   0% {
    //     -webkit-transform: translateY(-100%);
    //     transform: translateY(-100%);
    //     visibility: visible
    //   }
    //   100% {
    //     -webkit-transform: translateY(0);
    //     transform: translateY(0)
    //   }
    // }
         }

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