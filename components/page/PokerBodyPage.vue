<template>
   <div class="body-field">
        <div class="body-container-hot-game">
            <title-image :hrContainerTitle="hrContainerTitle" :CustomClassStyle="customClassStyle" :customClass="classStyle" :customComponent="condition" :title="title" :width="width" :height="height" />
        </div>

        <div class="card-content-sport">
            <card-game :customFourColumn="customFourColumn" :gridColunmCard="gridColunmCard" :cardMultiple="cardMultiple" :CardDataOneSlots="CardDataOneSlots" />
        </div>

         <div class="content-text">
            <content-text :width="widthContentText" :height="heightContentText" :ContentText="ContentText" />
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                widthContentText: "1024px",
                heightContentText: "60px",
                ContentText: 'Selamat datang di situs Sukabet,situs permainan online terlengkap dan terpercaya. Pada halaman ini anda dapat memilih kategori permainan yang anda ingin mainkan saat ini. Bagi anda yang belum memiliki akun, silahkan membuat akun dengan mengklik "Daftar" dan dapantkan bonus pemain baru di situs kami. Rasakan keseruan yang telah dirasakan oleh pemain lainnya. Jangan ketingalan permainan terbaru yang seru di situs kami. Kami hanya memiliki permainan-permainan terbaik agar anda tidak bingung',
                gridColunmCard: "four-column",
                cardMultiple: false,
                width: "25",
                height: "30",
                condition: true,
                title: "POKER",
                classStyle: "item-custom-poker",
                customClassStyle: true,
                hrContainerTitle: "hr-conatiner-title",
                customFourColumn: "custom-center-column",
                CardDataOneSlots: [
                    {
                        BALAKPLAY: { 
                            multipleImage: false,
                            cardTitle: false,
                            title: "BALAKPLAY",
                            classStyle: "maxbet-image",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-hot-game",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                        },
                        NINEGAMING: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "NINEGAMING",
                            classStyle: "co9-sport-image",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-hot-game",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                        },
                        IDNPOKER: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "IDNPOKER",
                            classStyle: "cmd-368-image",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-hot-game",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                        },
                        JAKAITAPOKER: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "JAKAITAPOKER",
                            classStyle: "pragmatic-play",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-hot-game",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
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
            @extend .btn-bg-red;
            @extend .border-radius-3px;
            margin: 10px 0px;
        }
        .card-content-sport {
            border-bottom: 1px solid $border-right-cr;
            padding: 0px 0px 20px 0px;
        }
        .content-text {
            padding: 0px 0px 20px 0px;
        }
    }
</style>