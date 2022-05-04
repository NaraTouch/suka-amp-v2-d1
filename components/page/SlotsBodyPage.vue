<template>
    <div class="slots-body">
        <!-- <div class="popup-style">
            <amp-lightbox class="z-index-style" id="modalbox" layout="nodisplay">
                <div class="modalbox">
                    <popup />
                </div>
            </amp-lightbox>
        </div> -->

        <div class="tap-container">
            <div class="body-container-sport">
                 <title-image :hrContainerTitle="hrContainerTitle" :CustomClassStyle="customClassStyle" :customClass="classStyleMenu" :customComponent="condition" :title="title"  />
            </div>

            <div class="filter-game first-tab-style">
                <button [class]="background" class="custom-btn btn-style btn-select" >SEMUA GAMES</button>
                <button class="custom-btn btn-style" on="tap:AMP.setState({ background: 'change-bg-br' })" >NEW GAMES</button>
                <button class="custom-btn btn-style">MOST PLAYED</button>
                <button class="custom-btn btn-style">WIN BOUNS</button>
                <button class="custom-btn btn-style">BIG PRICE</button>
            </div>
        </div>

        <div class="body-field">
            <section class="column-left">
                <amp-selector class="tabs-with-selector button-tab " role="tablist" on="select:myTabPanels.toggle(index=event.targetOption, value=true)" keyboard-select-mode="focus">
                    <div class="tab-style" id="sample3-tab1 " role="tab" aria-controls="sample3-tabpanel1" option="0" selected>
                        <title-image :customMenusStyle="customMenusStyle" :hrContainerTitle="hrContainerTitleHabanero" :CustomClassStyle="customClassStyleHabanero" :customClass="classStyle" :customComponent="condition" :title="titleHabanero" :spanStyle="spanStyle" />
                    </div>
                    <div v-for="(tabData, index) in tabDatas" :key="index">
                        <div v-for="(data, index) in tabData" :key="index">
                            <div  class="tab-style" :id="data.simpleTab" role="tab" :aria-controls="data.sampleTabpanel" :option="data.option">
                                <title-image 
                                :customMenusStyle="data.customMenusStyle"
                                :hrContainerTitle="data.hrContainerTitle" 
                                :CustomClassStyle="data.customClassStyle"
                                :customClass="data.classStyle" 
                                :customComponent="data.condition"
                                :title="data.title" 
                                :spanStyle="data.spanStyle" />
                            </div>
                        </div>
                    </div>
                </amp-selector>
            </section>

            <article class="column-right">
                <div class="tab-body">
                    <amp-selector id="myTabPanels" class="tabpanels">
                        <div id="sample3-tabpanel1" role="tabpanel" aria-labelledby="sample3-tab1" option selected>
                            <card-game :gridColunmCard="gridColunmCard" :slotsGames="slotsGames" :CardDataOneSlots="CardDataOneSlots" />
                        </div>
                        <div id="sample3-tabpanel2" role="tabpanel" aria-labelledby="sample3-tab2" option>Tab two content... </div>
                        <div id="sample3-tabpanel3" role="tabpanel" aria-labelledby="sample3-tab3" option>Tab three content... </div>
                        <div id="sample3-tabpanel4" role="tabpanel" aria-labelledby="sample3-tab4" option>Tab four content... </div>
                        <div id="sample3-tabpanel5" role="tabpanel" aria-labelledby="sample3-tab5" option>Tab five content... </div>
                        <div id="sample3-tabpanel6" role="tabpanel" aria-labelledby="sample3-tab6" option>Tab six content... </div>
                        <div id="sample3-tabpanel7" role="tabpanel" aria-labelledby="sample3-tab7" option>Tab seven content... </div>
                        <div id="sample3-tabpanel8" role="tabpanel" aria-labelledby="sample3-tab8" option>Tab eight content... </div>
                        <div id="sample3-tabpanel9" role="tabpanel" aria-labelledby="sample3-tab9" option>Tab nine content... </div>
                        <div id="sample3-tabpanel10" role="tabpanel" aria-labelledby="sample3-tab10" option>Tab ten content... </div>
                    </amp-selector>
                </div>

                <div class="content-text">
                    <content-text :width="widthContentText" :height="heightContentText" :ContentText="ContentText" />
                </div>
            </article>
        </div>
        
    </div>
</template>

<script>
    export default {
        components: { 
            CardGame: () => import('../card/CardGame'),
            ContentText: () => import('../content/ContentText'),
        },
        data() {
            return {
                title: "SLOTS",
                hrContainerTitle: "hr-conatiner-title",
                condition: true,
                customClassStyle: true,
                classStyleMenu: "item-custom-slots",

                // card-game
                slotsGames: true,
                gridColunmCard: "five-column",
                CardDataOneSlots: [
                    {
                        HABANERO: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "HABANERO",
                            classStyle: "game-image",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-slots",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                            loadingClick: true
                        },
                        MICROGMAING: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "MICROGMAING",
                            classStyle: "game-image",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-slots",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                            loadingClick: true
                        },
                        PRAGAMATICPLAY: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "MICROGMAING",
                            classStyle: "game-image",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-slots",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                            loadingClick: true
                        },
                        FISHINGKING: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "FISHINGKING",
                            classStyle: "game-image",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-slots",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                            loadingClick: true
                        },
                        PARADRSE: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "PARADRSE",
                            classStyle: "game-image",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-slots",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                            loadingClick: true
                        },
                        FISHINGWAR: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "FISHINGWAR",
                            classStyle: "game-image",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-slots",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",
                            loadingClick: true
                        },
                        GAMING: {
                            multipleImage: false,
                            cardTitle: false,
                            title: "GAMING",
                            classStyle: "game-image",
                            link: "https://www.w3schools.com/",
                            customimageClassStyle: "menus-slots",
                            btnTitle: "Main Sekarang",
                            btnStyle: "btn-style",  
                            loadingClick: true
                        },
                    }
                ],

                // tab-game
                customClassStyleHabanero: false,
                customMenusStyle: "menus-tab",
                spanStyle: "span-style",
                titleHabanero: "HABANERO",
                classStyle: "item-custom-habanero",
                hrContainerTitleHabanero: "hr-container-title-white",
                tabDatas: [
                    { 
                        MICROGMAING: {
                            customMenusStyle: "menus-tab",
                            title: "MICROGMAING",
                            classStyle: "item-custom-micro-gaming",
                            hrContainerTitle: "hr-container-title-white",
                            customClassStyle: false,
                            condition: true,
                            option: "1",
                            simpleTab: "sample3-tab2",
                            sampleTabpanel: "sample3-tabpanel2",
                            spanStyle: "span-style",
                        },
                        PRAGAMATICPLAY: {
                            customMenusStyle: "menus-tab",
                            title: "PRAGAMATIC PLAY",
                            classStyle: "item-custom-pragmatic-play",
                            hrContainerTitle: "hr-container-title-white",
                            customClassStyle: false,
                            condition: true,
                            option: "2",
                            simpleTab: "sample3-tab3",
                            sampleTabpanel: "sample3-tabpanel3",
                            spanStyle: "span-style"
                        },
                        POCKETGAMESSOFT: {
                            customMenusStyle: "menus-tab",
                            title: "POCKET GAMES SOFT",
                            classStyle: "item-custom-pocket-games-soft",
                            hrContainerTitle: "hr-container-title-white",
                            customClassStyle: false,
                            condition: true,
                            option: "3",
                            simpleTab: "sample3-tab4",
                            sampleTabpanel: "sample3-tabpanel4",
                            spanStyle: "span-style"
                        },
                        BIGGAMING: {
                            customMenusStyle: "menus-tab",
                            title: "BIG GAMING",
                            classStyle: "item-custom-big-gaming",
                            hrContainerTitle: "hr-container-title-white",
                            customClassStyle: false,
                            condition: true,
                            option: "4",
                            simpleTab: "sample3-tab5",
                            sampleTabpanel: "sample3-tabpanel5",
                            spanStyle: "span-style"
                        },
                        RTGSLOTS: {
                            customMenusStyle: "menus-tab",
                            title: "RTG SLOTS",
                            classStyle: "item-custom-rtg-slots",
                            hrContainerTitle: "hr-container-title-white",
                            customClassStyle: false,
                            condition: true,
                            option: "5",
                            simpleTab: "sample3-tab6",
                            sampleTabpanel: "sample3-tabpanel6",
                            spanStyle: "span-style"
                        },
                        JOKERGAMING: {
                            customMenusStyle: "menus-tab",
                            title: "JOKER GAMING",
                            classStyle: "item-custom-joker-gaming",
                            hrContainerTitle: "hr-container-title-white",
                            customClassStyle: false,
                            condition: true,
                            option: "6",
                            simpleTab: "sample3-tab7",
                            sampleTabpanel: "sample3-tabpanel7",
                            spanStyle: "span-style"
                        },
                        CQ9GAMING: {
                            customMenusStyle: "menus-tab",
                            title: "CQ9 GAMING",
                            classStyle: "item-custom-cq9-gaming",
                            hrContainerTitle: "hr-container-title-white",
                            customClassStyle: false,
                            condition: true,
                            option: "7",
                            simpleTab: "sample3-tab8",
                            sampleTabpanel: "sample3-tabpanel8",
                            spanStyle: "span-style"
                        },
                        SPADEGMAING: {
                            customMenusStyle: "menus-tab",
                            title: "SPADEGMAING",
                            classStyle: "item-custom-spade-gaming",
                            hrContainerTitle: "hr-container-title-white",
                            customClassStyle: false,
                            condition: true,
                            option: "8",
                            simpleTab: "sample3-tab9",
                            sampleTabpanel: "sample3-tabpanel9",
                            spanStyle: "span-style"
                        },
                        FLOWGAMING: {
                            customMenusStyle: "menus-tab",
                            title: "FLOW GAMING",
                            classStyle: "item-custom-flow-gaming",
                            hrContainerTitle: "hr-container-title-white",
                            customClassStyle: false,
                            condition: true,
                            option: "9",
                            simpleTab: "sample3-tab10",
                            sampleTabpanel: "sample3-tabpanel10",
                            spanStyle: "span-style"
                        },
                    }
                ],

                 // content-text
                widthContentText: "740px",
                heightContentText: "60px",
                ContentText: 'Selamat datang di situs Sukabet,situs permainan online terlengkap dan terpercaya. Pada halaman ini anda dapat memilih kategori permainan yang anda ingin mainkan saat ini. Bagi anda yang belum memiliki akun, silahkan membuat akun dengan mengklik "Daftar" dan dapantkan bonus pemain baru di situs kami. Rasakan keseruan yang telah dirasakan oleh pemain lainnya. Jangan ketingalan permainan terbaru yang seru di situs kami. Kami hanya memiliki permainan-permainan terbaik agar anda tidak bingung',
            }
        },
    }
</script>

<style lang="scss" amp-boilerplate>
    .slots-body {
        .tap-container {
            @extend .border-radius-3px;
            @extend .btn-bg-red;
            @extend .display-grid;
            background: url(/images/button/container-slots-btn.png);
            grid-template-columns: 1.1fr 3fr;
        }

        .first-tab-style {
            &:after {
                background-image: url(/images/button/testing.png);
                background-repeat: no-repeat;
                display: block;
                content: "";
                position: absolute;
                margin: -4px 0px 0px -2px;
                padding: 22px;
                background-size: contain;
            }
        }

        .filter-game {
            display: grid;
            grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
            margin: 5px 0px 0px 2px;

            .custom-btn {
                width: 148px;
                height: 40px;
                color: $color-white;
                padding: 10px 20px;
                cursor: pointer;
            }
            .btn-style {
                border: none;
                background: $color-gray;
                border-right: 1px solid $color-white;
                &:last-child {
                    border-right: 0px solid $color-white;
                    @extend .border-radius-3px;
                }

                &:active{
                    background: $tab-cr-border-bottom;
                }

                &:focus{
                    background: $tab-cr-border-bottom;
                }
            }

            .btn-select {
                background: $tab-cr-border-bottom;
            }

            .change-bg-br {
                border: none;
                background: $color-gray;
                color: $color-white;
                border-right: 1px solid $color-white;
                cursor: pointer;

                &:active{
                    background: $tab-cr-border-bottom;
                }

                &:focus{
                    background: $tab-cr-border-bottom;
                }
            }
        }

        .body-field {
            @extend .display-grid;
            grid-template-columns: 1.1fr 3fr;

            .tab-style {
                margin: 10px 0px;
            }
            .column-right {
                .tab-body {
                    margin-top: 10px;
                    border-bottom: 1px solid $border-right-cr;
                    padding: 0px 0px 20px 0px;
                }
                 .content-text {
                    @extend .contend-text-style;
                }
            }
        }
        
        .header-title {
            .title-card {
                margin: 5px 10px;
            }
        }
        
        amp-selector[role=tablist].tabs-with-flex [role=tab][selected] {
            outline: none;
        }
        amp-selector[role=tablist].tabs-with-flex [role=tabpanel] {
            display: none;
            width: 100%;
            order: 1; 
        }
        amp-selector[role=tablist].tabs-with-flex [role=tab][selected] + [role=tabpanel] {
            display: block;
        }

        amp-selector[role=tablist].tabs-with-selector {
            border-bottom-right-radius: 3px;
        }
        amp-selector[role=tablist].tabs-with-selector [role=tab][selected] {
            @extend .border-radius-3px;
            outline: none;
            background-color: #70757d;
        }
        amp-selector[role=tablist].tabs-with-selector {
            font-size: 12px;
        }
        amp-selector[role=tablist].tabs-with-selector [role=tab] {
            border-radius: 3px;
            background-color: #38383c;
            width: 100%;
            color: $color-white;
        }
        amp-selector.tabpanels [role=tabpanel] {
          display: none;
        }
        amp-selector.tabpanels [role=tabpanel][selected] {
          outline: none;
          display: block;
        }
    }
</style>