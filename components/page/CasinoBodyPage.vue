<template>
    <div class="body-field">
        <div class="body-container-casino">
            <title-image :hrContainerTitle="hrContainerTitle" :CustomClassStyle="customClassStyle" :customClass="classStyle" :customComponent="condition" :title="title" :width="width" :height="height" />
        </div>
        
        <div class="card-content-casino">
            <card-game :gridColunmCard="gridColunmCard" :cardMultiple="cardMultiple" :CardDataOneSlots="CardDataOneSlots" />
        </div>

        <div class="content-text">
            <content-text :width="widthContentText" :height="heightContentText" :ContentText="ContentText" />
        </div>
    </div>
</template>

<script>
    export default {
        components: {
            TabWinner: () => import('../Tab/TabWinner'),
                Slider: () => import('../slider/Slider'),
        },
         data() {
            return {
                widthContentText: "1024px",
                heightContentText: "60px",
                ContentText: 'Selamat datang di situs Sukabet,situs permainan online terlengkap dan terpercaya. Pada halaman ini anda dapat memilih kategori permainan yang anda ingin mainkan saat ini. Bagi anda yang belum memiliki akun, silahkan membuat akun dengan mengklik "Daftar" dan dapantkan bonus pemain baru di situs kami. Rasakan keseruan yang telah dirasakan oleh pemain lainnya. Jangan ketingalan permainan terbaru yang seru di situs kami. Kami hanya memiliki permainan-permainan terbaik agar anda tidak bingung',
                gridColunmCard: "five-column",
                cardMultiple: false,
                width: "25",
                height: "30",
                condition: true,
                title: "CASINO",
                classStyle: "item-custom-casino",
                customClassStyle: true,
                hrContainerTitle: "hr-conatiner-title",
                CardDataOneSlots: [
                    {
                        bgGame: { 
                            multipleImage: false,
                            cardTitle: false,
                            title: "DG",
                            classStyle: "maxbet-image",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-casino",
                            oneimageBodyCustom: "oneimage-body-custom",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                            buttonClick: true
                        },
                        idnGame: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "IDNGAME",
                            classStyle: "co9-sport-image",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-casino",
                            oneimageBodyCustom: "oneimage-body-custom",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                            buttonClick: true
                        },
                        C09Live: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "C09LIVE",
                            classStyle: "cmd-368-image",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-casino",
                            oneimageBodyCustom: "oneimage-body-custom",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                            buttonClick: true
                        },
                        HoGaming: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "HOGAMING",
                            classStyle: "ho-gaming",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-casino",
                            oneimageBodyCustom: "oneimage-body-custom",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                            buttonClick: true
                        },
                        DreamGaming: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "DREAM GAMING",
                            classStyle: "dream-gaming",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-casino",
                            oneimageBodyCustom: "oneimage-body-custom",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                            buttonClick: true
                        },
                        D88GreenDragon: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "D88 GREEN DRAGON",
                            classStyle: "green-dragon",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-casino",
                            oneimageBodyCustom: "oneimage-body-custom",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                            buttonClick: true
                        },
                        WWCasino: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "WW CASINO",
                            classStyle: "ww-casino",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-casino",
                            oneimageBodyCustom: "oneimage-body-custom",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                            buttonClick: true
                        },
                        ICONCasino: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "ICON CASINO",
                            classStyle: "icon-casino",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-casino",
                            oneimageBodyCustom: "oneimage-body-custom",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                            buttonClick: true
                        },
                        PragmaticPlay: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "PRAGMATIC PLAY",
                            classStyle: "pragmatic-play",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-casino",
                            oneimageBodyCustom: "oneimage-body-custom",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                            buttonClick: true
                        },
                        SBOBET: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "SBOBET",
                            classStyle: "sbobet",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-casino",
                            oneimageBodyCustom: "oneimage-body-custom",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                            buttonClick: true
                        },
                    }
                ],
            };
        },
    }
</script>

<style lang="scss" amp-boilerplate>
    .body-field { 
        .body-container-casino {
            @extend .body-container-style;
        }
        .card-content-casino {
           @extend .card-content-style;
        }
        .content-text {
           @extend .contend-text-style;
        }
    }
</style>