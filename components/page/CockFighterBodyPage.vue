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
            gridColunmCard: "two-column",
            cardMultiple: false,
            width: "25",
            height: "30",
            condition: true,
            title: "COCK FIGHTING",
            classStyle: "item-custom-cock-fighting",
            customClassStyle: true,
            hrContainerTitle: "hr-conatiner-title",
            customFourColumn: "custom-center-column",
            CardDataOneSlots: [
                {
                    S1288: { 
                        multipleImage: false,
                        cardTitle: false,
                        title: "S1288",
                        classStyle: "s1288-image",
                        link: "https://www.w3schools.com/",
                        customimageClassStyle: "menus-cock-fighting",
                        btnTitle: "Main Sekarang",
                        btnStyle: "btn-style",
                    },
                    SV388: {
                        multipleImage: false,
                        cardTitle: false,
                        title: "SV388",
                        classStyle: "sv388-image",
                        link: "https://www.w3schools.com/",
                        customimageClassStyle: "menus-cock-fighting",
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
        .body-container-arcade {
            @extend .btn-bg-red;
            @extend .border-radius-3px;
            margin: 10px 0px;
        }
        .card-content-arcade {
            border-bottom: 1px solid $border-right-cr;
            padding: 0px 0px 20px 0px;
        }
        .content-text {
            padding: 0px 0px 20px 0px;
        }
    }
</style>