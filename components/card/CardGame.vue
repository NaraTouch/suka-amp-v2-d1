<template>
    <div class="card-container" :class="customFourColumn" >
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
                        :btnTitle="data.btnTitle"
                        :buttonClick="data.buttonClick" />
                </div>
            </div>
        </div>

        <div v-if="slotsGames">
            <div  :class="gridColunmCard" v-for=" (CardDataOneSlot, index) in CardDataOneSlots" :key="index">
                <div class="mr-card" v-for=" (data, index) in CardDataOneSlot" :key="index">
                    <Card  
                        :multipleImage="data.multipleImage"
                        :cardTitle="data.cardTitle"
                        :linkButton="data.link"
                        :customClassImageOne="data.classStyle"
                        :customimageClassStyle="data.customimageClassStyle"
                        :oneimageBodyCustom="data.oneimageBodyCustom"
                        :btnTitle="data.btnTitle"
                        :btnStyle="data.btnStyle"
                        :loadingClick="data.loadingClick" />
                </div>
            </div>
        </div>

        <div v-else>
            <div  :class="gridColunmCard" v-for=" (CardDataOneSlot, index) in CardDataOneSlots" :key="index">
                <div class="mr-card" v-for=" (data, index) in CardDataOneSlot" :key="index">
                    <Card  
                        :multipleImage="data.multipleImage"
                        :cardTitle="data.cardTitle"
                        :linkButton="data.link"
                        :customClassImageOne="data.classStyle"
                        :customimageClassStyle="data.customimageClassStyle"
                        :oneimageBodyCustom="data.oneimageBodyCustom"
                        :btnTitle="data.btnTitle"
                        :btnStyle="data.btnStyle"
                        :buttonClick="data.buttonClick" />
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
            cardDatas: Array,
            gridColunmCard: String,
            customFourColumn: String,
            slotsGames: Boolean,
        },
        data() {
            return {
               
            }
        },
    }
</script>

<style lang="scss" amp-boilerplate>
    .card-container {
        .card-grid {
            @extend .display-grid;
            grid-template-columns: 1fr 1fr;
        }
        .five-column {
            @extend .display-grid;
            grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
        }
        .four-column {
            @extend .display-grid;
            grid-template-columns: 1fr 1fr 1fr 1fr;
        }
        .two-column {
            @extend .display-grid;
            grid-template-columns: 1fr 1fr;
        }
    }

    .custom-center-column {
        display: grid;
        place-items:  center;
    }
</style>