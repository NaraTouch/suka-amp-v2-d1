<template>
    <div class="card-container">
        <div class="card-left" v-for=" (cardDataLeft, index) in cardDataLefts" :key="index">
            <div class="mr-card" v-for=" (data, index) in cardDataLeft" :key="index">
            <Card  :title="data.title" :imageTitle="data.titleIcon"
            :imageBodyFirst="data.imageFirst" 
            :imageBodySecound="data.imageSecond"
            :linkButton="data.link" />
            </div>
        </div>

        <!-- <div class="card-right" v-for=" (cardDataRight, index) in cardDataRights" :key="index">
            <Card />
        </div>         -->
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
                        titleIcon: "/images/card/hot-game-image.png",
                        imageFirst: "/images/card/poker-thumb.png",
                        imageSecond: "/images/card/poker-thumb.png",
                        link: "https://www.w3schools.com/"
                    },
                    casinoGames: {
                        title: "Casino",
                        titleIcon: "/images/card/hot-game-image.png",
                        imageFirst: "/images/card/poker-thumb.png",
                        imageSecond: "/images/card/poker-thumb.png",
                        link: "https://www.w3schools.com/"
                    },
                    pokerGames: {
                        title: "Poker",
                        titleIcon: "/images/card/hot-game-image.png",
                        imageFirst: "/images/card/poker-thumb.png",
                        imageSecond: "/images/card/poker-thumb.png",
                        link: "https://www.w3schools.com/"
                    },
                    TogelGames: {
                        title: "Togel",
                        titleIcon: "/images/card/hot-game-image.png",
                        imageFirst: "/images/card/poker-thumb.png",
                        imageSecond: "/images/card/poker-thumb.png",
                        link: "https://www.w3schools.com/"
                    },
                }
            ],
            cardDataRights: [
                {
                    sportsGames: {
                        title: "Sorts",
                        titleIcon: "",
                        imageFirst: "",
                        imageSecond: "",
                        link: "link"
                    },
                    slotsGames: {
                        title: "Slots",
                        titleIcon: "",
                        imageFirst: "",
                        imageSecond: "",
                        link: "link"
                    },
                     arcadeGames: {
                        title: "Arcade",
                        titleIcon: "",
                        imageFirst: "",
                        imageSecond: "",
                        link: "link"
                    },
                    cockFightingGames: {
                        title: "Cock Fighting",
                        titleIcon: "",
                        imageFirst: "",
                        imageSecond: "",
                        link: "link"
                    },
                }
            ]
        }
    },
}
</script>

<style lang="scss">
    .card-container {
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-gap: 10px;

        .card-left {    
            .mr-card {
                margin-bottom: 10px;
            }
        }
        .card-right {

        }

    }
        
</style>