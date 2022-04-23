<template>
    <div class="card-container">
        <div class="card-grid" v-for=" (cardDataLeft, index) in cardDataLefts" :key="index">
            <div class="mr-card" v-for=" (data, index) in cardDataLeft" :key="index">
                <Card  
                    :title="data.title" 
                    :linkButton="data.link" 
                    :customClassImageTitle="data.classStyle"
                    :customClassFirst="data.customClassFirst"
                    :customClassSecond="data.customClassSecond" />
            </div>
        </div>
    </div>
</template>

<script>
export default {
    components: {
        Card: () => import('../card/Card'),
    },
    data() {
        return {
            cardDataLefts: [
                { 
                    hotGames: {
                        title: "Hot Games",
                        link: "https://www.w3schools.com/",
                        customClassFirst: "item-custom-hot-game-first",
                        customClassSecond: "item-custom-hot-game-second",
                        classStyle: "item-custom-hot-game",
                    },
                    sportsGames: {
                        title: "Sports",
                        link: "https://www.w3schools.com/",
                        customClassFirst: "item-custom-sports-first",
                        customClassSecond: "item-custom-sports-second",
                        classStyle: "item-custom-sports",
                    },
                    casinoGames: {
                        title: "Casino",
                        link: "https://www.w3schools.com/",
                        customClassFirst: "item-custom-casino-first",
                        customClassSecond: "item-custom-casino-second",
                        classStyle: "item-custom-casino",
                    },
                    slotsGames: {
                        title: "Slots",
                        link: "https://www.w3schools.com/",
                        customClassFirst: "item-custom-slots-first",
                        customClassSecond: "item-custom-slots-second",
                        classStyle: "item-custom-slots",
                    },
                    pokerGames: {
                        title: "Poker",
                        link: "https://www.w3schools.com/",
                        customClassFirst: "item-custom-poker-first",
                        customClassSecond: "item-custom-poker-second",
                        classStyle: "item-custom-poker",
                    },
                    arcadeGames: {
                        title: "Arcade",
                        link: "https://www.w3schools.com/",
                        customClassFirst: "item-custom-arcade-first",
                        customClassSecond: "item-custom-arcade-second",
                        classStyle: "item-custom-arcade",
                    },
                    TogelGames: {
                        title: "Togel",
                        link: "https://www.w3schools.com/",
                        customClassFirst: "item-custom-togel-first",
                        customClassSecond: "item-custom-togel-second",
                        classStyle: "item-custom-togel",
                    },
                    cockFightingGames: {
                        title: "Cock Fighting",
                        link: "https://www.w3schools.com/",
                        customClassFirst: "item-custom-cock-fighting-first",
                        customClassSecond: "item-custom-cock-fighting-second",
                        classStyle: "item-custom-cock-fighting",
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
    }
</style>