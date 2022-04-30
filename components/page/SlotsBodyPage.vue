<template>
    <div class="slots-body">
        <div class="tap-container">
            <div class="body-container-sport">
                 <title-image :hrContainerTitle="hrContainerTitle" :CustomClassStyle="customClassStyle" :customClass="classStyleMenu" :customComponent="condition" :title="title"  />
            </div>

            <div class="filter-game">
                <button class="custom-btn btn-style">Read Moress</button>
                <button class="custom-btn btn-style">NEW GAMES</button>
                <button class="custom-btn btn-style">MOST PLAYED</button>
                <button class="custom-btn btn-style">WIN BOUNS</button>
                <button class="custom-btn btn-style">BIG PRICE</button>
            </div>
        </div>

        <div class="body-field">
            <section class="column-left">
                <amp-selector class="tabs-with-selector button-tab " role="tablist" on="select:myTabPanels.toggle(index=event.targetOption, value=true)" keyboard-select-mode="focus">
                    <div class="tab-style first-tab-style" id="sample3-tab1 " role="tab" aria-controls="sample3-tabpanel1" option="0" selected>
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
                <div class="test">
                    <amp-selector id="myTabPanels" class="tabpanels">
                        <div id="sample3-tabpanel1" role="tabpanel" aria-labelledby="sample3-tab1" option selected>Tab one content... </div>
                        <div id="sample3-tabpanel2" role="tabpanel" aria-labelledby="sample3-tab2" option>Tab two content... </div>
                        <div id="sample3-tabpanel3" role="tabpanel" aria-labelledby="sample3-tab3" option>Tab three content... </div>
                        <div id="sample3-tabpanel4" role="tabpanel" aria-labelledby="sample3-tab4" option>Tab four content... </div>
                        <div id="sample3-tabpanel5" role="tabpanel" aria-labelledby="sample3-tab5" option>Tab five content... </div>
                        <div id="sample3-tabpanel6" role="tabpanel" aria-labelledby="sample3-tab6" option selected>Tab six content... </div>
                        <div id="sample3-tabpanel7" role="tabpanel" aria-labelledby="sample3-tab7" option>Tab seven content... </div>
                        <div id="sample3-tabpanel8" role="tabpanel" aria-labelledby="sample3-tab8" option>Tab eight content... </div>
                        <div id="sample3-tabpanel9" role="tabpanel" aria-labelledby="sample3-tab9" option>Tab nine content... </div>
                        <div id="sample3-tabpanel10" role="tabpanel" aria-labelledby="sample3-tab10" option>Tab ten content... </div>
                    </amp-selector>
                </div>
            </article>
        </div>

    </div>
</template>

<script>
    export default {
        data() {
            return {
                title: "SLOTS",
                hrContainerTitle: "hr-conatiner-title",
                condition: true,
                customClassStyle: true,
                classStyleMenu: "item-custom-slots",

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
            }
        },
    }
</script>

<style lang="scss" amp-boilerplate>
    .slots-body {
        .tap-container {
            @extend .border-radius-3px;
            @extend .btn-bg-red;
            background: url(/images/button/container-slots-btn.png);
            display: grid;
            grid-template-columns: 1.1fr 3fr;
            grid-gap: 10px;
        }

        .filter-game {
            display: grid;
            grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
            margin: 5px 0px 0px 0px;

            .custom-btn {
                width: 148px;
                height: 40px;
                color: #fff;
                padding: 10px 25px;
                background: transparent;
                cursor: pointer;
                
                // transition: all 0.3s ease;
                // position: relative;
                // display: inline-block;
                // box-shadow:inset 2px 2px 2px 0px rgba(255,255,255,.5),
                // 7px 7px 20px 0px rgba(0,0,0,.1),
                // 4px 4px 5px 0px rgba(0,0,0,.1);
                // outline: none;
            }
            .btn-style {
                border: none;
                background: rgb(251,33,117);
                background: linear-gradient(0deg, rgba(251,33,117,1) 0%, rgba(234,76,137,1) 100%);
                border-right: 1px solid white;
                &:last-child {
                    border-right: 0px solid white;
                }
            }
            // .btn-style:hover {
            //     text-decoration: none;
            //     color: #fff;
            // }
            // .btn-style:before {
            //     position: absolute;
            //     content: '';
            //     display: inline-block;
            //     top: -180px;
            //     left: 0;
            //     width: 30px;
            //     height: 100%;
            //     background-color: #fff;
            //     animation: shiny-btn1 3s ease-in-out infinite;
            // }
            // .btn-11:active{
            //     background:olive;
            // }

            // .btn-11:focus{
            //     background:olive;
            // }

            // .btn-11:hover{
            // opacity: .7;
            // }
            .btn-11:active{
            // box-shadow:  4px 4px 6px 0 rgba(255,255,255,.3),
            //             -4px -4px 6px 0 rgba(116, 125, 136, .2), 
            //     inset -4px -4px 6px 0 rgba(255,255,255,.2),
            //     inset 4px 4px 6px 0 rgba(0, 0, 0, .2);
            }


            // @-webkit-keyframes shiny-btn1 {
            //     0% { -webkit-transform: scale(0) rotate(45deg); opacity: 0; }
            //     80% { -webkit-transform: scale(0) rotate(45deg); opacity: 0.5; }
            //     81% { -webkit-transform: scale(4) rotate(45deg); opacity: 1; }
            //     100% { -webkit-transform: scale(50) rotate(45deg); opacity: 0; }
            // }
        }

        .body-field {
            display: grid;
            grid-template-columns: 1.1fr 3fr;
            grid-gap: 10px;

            .tab-style {
                margin: 10px 0px;
            }
        }
        
        // title-tab container
        .header-title {
            .title-card {
                margin: 5px 10px;
            }
        }
        
        // tab style 
        amp-selector[role=tablist].tabs-with-flex {
            // display: flex;
            flex-wrap: wrap;
        }
        amp-selector[role=tablist].tabs-with-flex [role=tab] {
            flex-grow: 1;
            // text-align: center;
        }
        amp-selector[role=tablist].tabs-with-flex [role=tab][selected] {
            outline: none;
            // background-image: url(/images/button/btn-tab.png);
            // @extend .bg-size-repeat; 
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
            // display: flex;
            // background-image: url(/images/button/btn-tabs.png);
            // @extend .bg-size-repeat;  
            border-bottom-right-radius: 3px;
        }
        amp-selector[role=tablist].tabs-with-selector [role=tab][selected] {
            outline: none;
            // background-image: url(/images/button/btn-tab.png);
            // @extend .bg-size-repeat; 
            border-radius: 3px;
            background-color: #70757d;
        }
        amp-selector[role=tablist].tabs-with-selector {
            // display: flex;
            font-size: 12px;
        }
        amp-selector[role=tablist].tabs-with-selector [role=tab] {
            // background-image: url(/images/button/btn-tabs.png);
            // @extend .bg-size-repeat;  
            border-radius: 3px;
            background-color: #38383c;
            width: 100%;
        //   text-align: center;
          color: white;
        }
        amp-selector.tabpanels [role=tabpanel] {
          display: none;
        }
        amp-selector.tabpanels [role=tabpanel][selected] {
          outline: none;
          display: block;
        }
    }
    // .slots-body {
    //     .button-tab {
    //         margin-top: 5px;

    //         .tab-style {
    //             border-right: 1px solid $text-color-1;
    //             padding: 13px;

    //             &:last-child {
    //                 border-right: none;
    //                 @extend .border-radius-3px;
    //             }
    //         }

    //         .first-tab-style {
    //             &:after {
    //                 background-image: url(/images/button/testing.png);
    //                 background-repeat: no-repeat;
    //                 display: block;
    //                 content: "";
    //                 position: absolute;
    //                 margin: -31px 0px 0px -14px;
    //                 padding: 22px;
    //                 background-size: contain;
    //             }
    //         }
    //     }

    //     amp-selector[role=tablist].tabs-with-flex {
    //         display: flex;
    //         flex-wrap: wrap;
    //     }
    //     amp-selector[role=tablist].tabs-with-flex [role=tab] {
    //         flex-grow: 1;
    //         text-align: center;
    //     }
    //     amp-selector[role=tablist].tabs-with-flex [role=tab][selected] {
    //         outline: none;
    //         background-image: url(/images/button/btn-tab.png);
    //         @extend .bg-size-repeat; 
    //     }
    //     amp-selector[role=tablist].tabs-with-flex [role=tabpanel] {
    //         display: none;
    //         width: 100%;
    //         order: 1; 
    //     }
    //     amp-selector[role=tablist].tabs-with-flex [role=tab][selected] + [role=tabpanel] {
    //         display: block;
            
    //     }

    //     amp-selector[role=tablist].tabs-with-selector {
    //         display: flex;
    //         background-image: url(/images/button/btn-tabs.png);
    //         @extend .bg-size-repeat;  
    //         border-bottom-right-radius: 3px;
    //     }
    //     amp-selector[role=tablist].tabs-with-selector [role=tab][selected] {
    //         outline: none;
    //         background-image: url(/images/button/btn-tab.png);
    //         @extend .bg-size-repeat; 
    //     }
    //     amp-selector[role=tablist].tabs-with-selector {
    //         display: flex;
    //         font-size: 12px;
    //     }
    //     amp-selector[role=tablist].tabs-with-selector [role=tab] {
    //       width: 100%;
    //       text-align: center;
    //       color: white;
    //     }
    //     amp-selector.tabpanels [role=tabpanel] {
    //       display: none;
    //     }
    //     amp-selector.tabpanels [role=tabpanel][selected] {
    //       outline: none;
    //       display: block;
    //     }

    //     .tap-container {
    //         @extend .border-radius-3px;
    //         @extend .btn-bg-red;
    //         background: url(/images/button/container-slots-btn.png);
    //         display: grid;
    //         grid-template-columns: 1.1fr 3fr;
    //         // grid-gap: 10px;
    //     }

    //     .body-field {
    //         @extend .display-flex;
    //         margin: 10px 0px 30px 0px;

    //         .border-row {
    //             @extend .z-index-1;
    //             padding: 0px 13px 0px 0px;
    //             margin: 0px -16px 0px 0px;
    //             position: relative;

    //             &:before {
    //                 @extend .border-right;
    //                 content: "";
    //                 position: absolute;
    //                 bottom: 112px;
    //                 right: 0;
    //                 height: 87%;
    //             }
    //         }

    //         .column-left {
    //             min-width: 265px;
    //             // padding-right: 15px;
    //             padding-right: 5px;

    //             .tab-winner {
    //                 border-bottom-right-radius: 4px;
    //             }

    //             .slider-promotion {
    //                 @extend .mr-box;
    //             }

    //             .stay-connected {
    //                 margin-bottom: 30px;
    //                 background-color: $bg-body-field;
    //                 @extend .border-radius-3px;
    //             }

    //             .payment-method {
    //                 padding-bottom: 15px;
    //                 @extend .border-radius-3px;
    //                 background-color: $bg-body-field;
    //             }

    //             .content-text {
    //                 margin-top: 20px;
    //             }
    //         }

    //         .column-right {
    //             min-width: 760px;
    //             padding-right: 5px;
                
    //             .body-container-sport {
    //                 @extend .btn-bg-red;
    //                 @extend .border-radius-3px;
    //             }

    //             .card-content-sport {
    //                 border-bottom: 1px solid $border-right-cr;
    //                 padding-bottom: 10px;
    //             }
    //         }
    //     }
    // }
</style>