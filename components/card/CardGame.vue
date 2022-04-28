<template>
    <div class="card-container">
        <div v-if="cardMultiple">
            <div class="card-grid" v-for=" (cardData, index) in cardDatas" :key="index">
                <div class="mr-card" v-for=" (data, index) in cardData" :key="index">
                    <Card  
                        :multipleImage="data.multipleImage"
                        :cardTitle="data.cardTitle"
                        :title="data.title" 
                        :linkButton="data.link" 
                        :customClassImageTitle="data.classStyle"
                        :customClassFirst="data.customClassFirst"
                        :customClassSecond="data.customClassSecond"
                        :btnTitle="data.btnTitle" />
                </div>
            </div>
        </div>

        <div v-else>
            <div  class="card-grid-one-image" v-for=" (CardDataOneSlot, index) in CardDataOneSlots" :key="index">
                <div class="mr-card" v-for=" (data, index) in CardDataOneSlot" :key="index">
                    <Card  
                        :multipleImage="data.multipleImage"
                        :cardTitle="data.cardTitle"
                        :linkButton="data.link"
                        :customClassImageOne="data.classStyle"
                        :customimageClassStyle="data.customimageClassStyle"
                        :oneimageBodyCustom="data.oneimageBodyCustom"
                        :btnTitle="data.btnTitle"
                        :btnStyle="data.btnStyle" />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        components: {
            Card: () => import('../card/Card'),
        },
        props: {
            cardMultiple: Boolean,
            CardDataOneSlots: Array,
            customimageClassStyle: String,
            oneimageBodyCustom: String,
        },
        data() {
            return {
                cardDatas: [
                    { 
                        hotGames: {
                            multipleImage: true,
                            cardTitle: true,
                            title: "Hot Games",
                            link: "https://www.w3schools.com/",
                            customClassFirst: "item-custom-hot-game-first",
                            customClassSecond: "item-custom-hot-game-second",
                            classStyle: "item-custom-hot-game",
                            btnTitle: "Lihat Semua"
                        },
                        sportsGames: {
                            multipleImage: true,
                            cardTitle: true,
                            title: "Sports",
                            link: "https://www.w3schools.com/",
                            customClassFirst: "item-custom-sports-first",
                            customClassSecond: "item-custom-sports-second",
                            classStyle: "item-custom-sports",
                            btnTitle: "Lihat Semua",
                        },
                        casinoGames: {
                            multipleImage: true,
                            cardTitle: true,
                            title: "Casino",
                            link: "https://www.w3schools.com/",
                            customClassFirst: "item-custom-casino-first",
                            customClassSecond: "item-custom-casino-second",
                            classStyle: "item-custom-casino",
                            btnTitle: "Lihat Semua",
                        },
                        slotsGames: {
                            multipleImage: true,
                            cardTitle: true,
                            title: "Slots",
                            link: "https://www.w3schools.com/",
                            customClassFirst: "item-custom-slots-first",
                            customClassSecond: "item-custom-slots-second",
                            classStyle: "item-custom-slots",
                            btnTitle: "Lihat Semua",
                        },
                        pokerGames: {
                            multipleImage: true,
                            cardTitle: true,
                            title: "Poker",
                            link: "https://www.w3schools.com/",
                            customClassFirst: "item-custom-poker-first",
                            customClassSecond: "item-custom-poker-second",
                            classStyle: "item-custom-poker",
                            btnTitle: "Lihat Semua",
                        },
                        arcadeGames: {
                            multipleImage: true,
                            cardTitle: true,
                            title: "Arcade",
                            link: "https://www.w3schools.com/",
                            customClassFirst: "item-custom-arcade-first",
                            customClassSecond: "item-custom-arcade-second",
                            classStyle: "item-custom-arcade",
                            btnTitle: "Lihat Semua",
                        },
                        TogelGames: {
                            multipleImage: true,
                            cardTitle: true,
                            title: "Togel",
                            link: "https://www.w3schools.com/",
                            customClassFirst: "item-custom-togel-first",
                            customClassSecond: "item-custom-togel-second",
                            classStyle: "item-custom-togel",
                            btnTitle: "Lihat Semua",
                        },
                        cockFightingGames: {
                            multipleImage: true,
                            cardTitle: true,
                            title: "Cock Fighting",
                            link: "https://www.w3schools.com/",
                            customClassFirst: "item-custom-cock-fighting-first",
                            customClassSecond: "item-custom-cock-fighting-second",
                            classStyle: "item-custom-cock-fighting",
                            btnTitle: "Lihat Semua",
                        },
                    }
                ],
            }
        },
    }
</script>

<style lang="scss" amp-boilerplate>
    .card-container {
        .card-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            grid-gap: 10px;
        }
        .card-grid-one-image {
            display: grid;
            grid-template-columns: 1fr 1fr 1fr 1fr;
            grid-gap: 10px;
            margin-top: 10px;
        }
    }
</style>