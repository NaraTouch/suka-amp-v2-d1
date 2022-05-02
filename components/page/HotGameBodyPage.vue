<template>
    <div class="body-field">
        <div class="body-container-hot-game">
            <title-image :hrContainerTitle="hrContainerTitle" :CustomClassStyle="customClassStyle" :customClass="classStyle" :customComponent="condition" :title="title" :width="width" :height="height" />
        </div>

        <div class="card-content-hot-game">
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
                title: "HOT GAMES",
                classStyle: "item-custom-hot-game",
                customClassStyle: true,
                hrContainerTitle: "hr-conatiner-title",
                CardDataOneSlots: [
                    {
                        BANDARBACCARAT: { 
                            multipleImage: false,
                            cardTitle: false,
                            title: "BANDARBACCARAT",
                            classStyle: "maxbet-image",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-hot-game",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                            buttonClick: true
                        },
                        BANDARCAPSA: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "BANDARCAPSA",
                            classStyle: "co9-sport-image",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-hot-game",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                            buttonClick: true
                        },
                        DOMINO: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "DOMINO",
                            classStyle: "cmd-368-image",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-hot-game",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                            buttonClick: true
                        },
                        CAPSASUSUN: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "CAPSASUSUN",
                            classStyle: "pragmatic-play",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-hot-game",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                            buttonClick: true
                        },
                        BANDARCEME: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "BANDARCEME",
                            classStyle: "sbobet",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-hot-game",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                            buttonClick: true
                        },
                    }
                ],
            }
        },
    }
</script>

<style lang="scss" amp-boilerplate>
    .body-field {
        .body-container-hot-game {
            @extend .body-container-style;
        }
        .card-content-hot-game {
            @extend .card-content-style;
        }
        .content-text {
            @extend .contend-text-style;
        }
    }
</style>