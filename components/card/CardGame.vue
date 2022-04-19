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

        <div class="card-right" v-for=" (cardDataRight, index) in cardDataRights" :key="index">
            <div class="mr-card" v-for=" (data, index) in cardDataRight" :key="index">
                <Card  :title="data.title" :imageTitle="data.titleIcon"
                :imageBodyFirst="data.imageFirst" 
                :imageBodySecound="data.imageSecond"
                :linkButton="data.link" />
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
                        titleIcon: "/images/card/hot-game-image.png",
                        imageFirst: "/images/card/poker-thumb.png",
                        imageSecond: "/images/card/poker-thumb.png",
                        link: "https://www.w3schools.com/"
                    },
                    slotsGames: {
                        title: "Slots",
                        titleIcon: "/images/card/hot-game-image.png",
                        imageFirst: "/images/card/poker-thumb.png",
                        imageSecond: "/images/card/poker-thumb.png",
                        link: "https://www.w3schools.com/"
                    },
                     arcadeGames: {
                        title: "Arcade",
                        titleIcon: "/images/card/hot-game-image.png",
                        imageFirst: "/images/card/poker-thumb.png",
                        imageSecond: "/images/card/poker-thumb.png",
                        link: "https://www.w3schools.com/"
                    },
                    cockFightingGames: {
                        title: "Cock Fighting",
                        titleIcon: "/images/card/hot-game-image.png",
                        imageFirst: "/images/card/poker-thumb.png",
                        imageSecond: "/images/card/poker-thumb.png",
                        link: "https://www.w3schools.com/"
                    },
                }
            ]
        }
    },
}
</script>

<style lang="scss">
    .card-container {
        @extend .display-grid;
        grid-template-columns: 1fr 1fr;
        
        .mr-card {
            margin-bottom: 10px;
            &:last-child {
                margin-bottom: 0px;
            }
        }
    }
        
</style>