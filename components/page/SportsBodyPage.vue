<template>
    <div class="body-field">
         <div class="body-container-sport">
            <title-image :hrContainerTitle="hrContainerTitle" :CustomClassStyle="customClassStyle" :customClass="classStyle" :customComponent="condition" :title="title" :width="width" :height="height" />
        </div>
        
        <div class="card-content-sport">
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
                title: "SPORTS",
                classStyle: "item-custom-sports",
                customClassStyle: true,
                hrContainerTitle: "hr-conatiner-title",
                CardDataOneSlots: [
                    {
                        MaxBetGame: { 
                            multipleImage: false,
                            cardTitle: false,
                            title: "MAXBET",
                            classStyle: "maxbet-image",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-sport",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                        },
                        CO9: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "CO9",
                            classStyle: "co9-sport-image",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-sport",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                        },
                        CMD368: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "CMD368",
                            classStyle: "cmd-368-image",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-sport",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                        },
                        PRAGMATICPLAY: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "PRAGMATIC PLAY",
                            classStyle: "pragmatic-play",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-sport",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                        },
                        SBOBET: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "TESTING",
                            classStyle: "sbobet",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-sport",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                        },
                    }
                ],
            };
        },
    }
</script>

<style lang="scss" amp-boilerplate>
    .body-field { 
        .body-container-sport {
            @extend .body-container-style;
        }

        .card-content-sport {
            @extend .card-content-style;
        }
        .content-text {
            @extend .contend-text-style;
        }
    }
    
</style>