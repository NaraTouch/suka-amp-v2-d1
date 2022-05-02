<template>
   <div class="body-field">
        <div class="body-container-arcade">
            <title-image :hrContainerTitle="hrContainerTitle" :CustomClassStyle="customClassStyle" :customClass="classStyle" :customComponent="condition" :title="title" :width="width" :height="height" />
        </div>
        
        <div class="card-content-arcade">
            <card-game :gridColunmCard="gridColunmCard" :cardMultiple="cardMultiple" :CardDataOneSlots="CardDataOneSlots" />
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
            gridColunmCard: "five-column",
            cardMultiple: false,
            width: "25",
            height: "30",
            condition: true,
            title: "ARCADE",
            classStyle: "item-custom-arcade",
            customClassStyle: true,
            hrContainerTitle: "hr-conatiner-title",
            CardDataOneSlots: [
                {
                    FORTUREFISHING: { 
                        multipleImage: false,
                        cardTitle: false,
                        title: "FORTUREFISHING",
                        classStyle: "forture-fishing-image",
                        link: "https://www.w3schools.com/",
                        customimageClassStyle: "menus-arcade",
                        btnTitle: "Main Sekarang",
                        btnStyle: "btn-style",
                        buttonClick: true
                    },
                    FISHCATCH: {
                        multipleImage: false,
                        cardTitle: false,
                        title: "FISHCATCH",
                        classStyle: "fish-catch-image",
                        link: "https://www.w3schools.com/",
                        customimageClassStyle: "menus-arcade",
                        btnTitle: "Main Sekarang",
                        btnStyle: "btn-style",
                        buttonClick: true
                    },
                    FISHINGKING: {
                        multipleImage: false,
                        cardTitle: false,
                        title: "FISHINGKING",
                        classStyle: "fish-king-image",
                        link: "https://www.w3schools.com/",
                        customimageClassStyle: "menus-arcade",
                        btnTitle: "Main Sekarang",
                        btnStyle: "btn-style",
                        buttonClick: true
                    },
                    PARADRSE: {
                        multipleImage: false,
                        cardTitle: false,
                        title: "PARADRSE",
                        classStyle: "paradrse-play",
                        link: "https://www.w3schools.com/",
                        customimageClassStyle: "menus-arcade",
                        btnTitle: "Main Sekarang",
                        btnStyle: "btn-style",
                        buttonClick: true
                    },
                    FISHINGWAR: {
                        multipleImage: false,
                        cardTitle: false,
                        title: "FISHINGWAR",
                        classStyle: "fishing-war-play",
                        link: "https://www.w3schools.com/",
                        customimageClassStyle: "menus-arcade",
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
        .body-container-arcade {
            @extend .body-container-style;
        }
        .card-content-arcade {
            @extend .card-content-style;
        }
        .content-text {
            @extend .contend-text-style;
        }
    }
</style>