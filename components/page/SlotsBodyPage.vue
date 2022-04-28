<template>
    <div class="slots-body">
        <div class="tap-container">
            <div class="body-container-sport">
                 <title-image :hrContainerTitle="hrContainerTitle" :CustomClassStyle="customClassStyle" :customClass="classStyle" :customComponent="condition" :title="title" :width="width" :height="height" />
            </div>

            <div>
                <amp-selector class="tabs-with-selector button-tab " role="tablist" on="select:myTabPanels.toggle(index=event.targetOption, value=true)" keyboard-select-mode="focus">
                    <div class="tab-style first-tab-style" id="sample3-tab1 " role="tab" aria-controls="sample3-tabpanel1" option="0" selected>SEMUA GAMES</div>
                    <div class="tab-style" id="sample3-tab2 " role="tab" aria-controls="sample3-tabpanel2" option="1">NEW GAMES</div>
                    <div class="tab-style" id="sample3-tab3 " role="tab" aria-controls="sample3-tabpanel3" option="2">MOST PLAYED</div>
                    <div class="tab-style" id="sample3-tab4" role="tab" aria-controls="sample3-tabpanel4" option="3">WIN BOUNS</div>
                    <div class="tab-style" id="sample3-tab5" role="tab" aria-controls="sample3-tabpanel5" option="4">BIG PRICE</div>
                </amp-selector>
            </div>
        </div>
        <div class="body-field">
            
            <section class="column-left">
                <title-image :hrContainerTitle="hrContainerTitle" :CustomClassStyle="customClassStyle" :customClass="classStyle" :customComponent="condition" :title="title" :width="width" :height="height" />  
            </section>
            <article class="column-right">
                <div class="test">
                    <amp-selector id="myTabPanels" class="tabpanels">
                        <div id="sample3-tabpanel1" role="tabpanel" aria-labelledby="sample3-tab1" option selected>Tab one content... </div>
                        <div id="sample3-tabpanel2" role="tabpanel" aria-labelledby="sample3-tab2" option>Tab two content... </div>
                        <div id="sample3-tabpanel3" role="tabpanel" aria-labelledby="sample3-tab3" option>Tab three content... </div>
                        <div id="sample3-tabpanel4" role="tabpanel" aria-labelledby="sample3-tab4" option>Tab four content... </div>
                        <div id="sample3-tabpanel5" role="tabpanel" aria-labelledby="sample3-tab5" option>Tab five content... </div>
                    </amp-selector>
                </div>
            </article>
        </div>
    </div>
</template>

<script>
    export default {
        components: { 
            TitleImage: () => import('../TitleImage'),
            TabSLotsGame : () =>import('../Tab/TabSLotsGame'),
        },
        data() {
            return {
                width: "25",
                height: "30",
                condition: true,
                customClassStyle: true,
                spanStyle: "span-style",
                title: "SLOTS",
                classStyle: "item-custom-slots",
                hrContainerTitle: "hr-conatiner-title",
            }
        },
    }
</script>

<style lang="scss" amp-boilerplate>
    .slots-body {
        .button-tab {
            margin-top: 5px;

            .tab-style {
                border-right: 1px solid $text-color-1;
                padding: 13px;

                &:last-child {
                    border-right: none;
                    @extend .border-radius-3px;
                }
            }

            .first-tab-style {
                &:after {
                    background-image: url(/images/button/testing.png);
                    background-repeat: no-repeat;
                    display: block;
                    content: "";
                    position: absolute;
                    margin: -31px 0px 0px -14px;
                    padding: 22px;
                    background-size: contain;
                }
            }
        }

        amp-selector[role=tablist].tabs-with-flex {
            display: flex;
            flex-wrap: wrap;
        }
        amp-selector[role=tablist].tabs-with-flex [role=tab] {
            flex-grow: 1;
            text-align: center;
        }
        amp-selector[role=tablist].tabs-with-flex [role=tab][selected] {
            outline: none;
            background-image: url(/images/button/btn-tab.png);
            @extend .bg-size-repeat; 
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
            display: flex;
            background-image: url(/images/button/btn-tabs.png);
            @extend .bg-size-repeat;  
            border-bottom-right-radius: 3px;
        }
        amp-selector[role=tablist].tabs-with-selector [role=tab][selected] {
            outline: none;
            background-image: url(/images/button/btn-tab.png);
            @extend .bg-size-repeat; 
        }
        amp-selector[role=tablist].tabs-with-selector {
            display: flex;
            font-size: 12px;
        }
        amp-selector[role=tablist].tabs-with-selector [role=tab] {
          width: 100%;
          text-align: center;
          color: white;
        }
        amp-selector.tabpanels [role=tabpanel] {
          display: none;
        }
        amp-selector.tabpanels [role=tabpanel][selected] {
          outline: none;
          display: block;
        }

        .tap-container {
            @extend .border-radius-3px;
            @extend .btn-bg-red;
            background: url(/images/button/container-slots-btn.png);
            display: grid;
            grid-template-columns: 1.1fr 3fr;
            // grid-gap: 10px;
        }

        .body-field {
            @extend .display-flex;
            margin: 10px 0px 30px 0px;

            .border-row {
                @extend .z-index-1;
                padding: 0px 13px 0px 0px;
                margin: 0px -16px 0px 0px;
                position: relative;

                &:before {
                    @extend .border-right;
                    content: "";
                    position: absolute;
                    bottom: 112px;
                    right: 0;
                    height: 87%;
                }
            }

            .column-left {
                min-width: 265px;
                padding-right: 15px;

                .tab-winner {
                    border-bottom-right-radius: 4px;
                }

                .slider-promotion {
                    @extend .mr-box;
                }

                .stay-connected {
                    margin-bottom: 30px;
                    background-color: $bg-body-field;
                    @extend .border-radius-3px;
                }

                .payment-method {
                    padding-bottom: 15px;
                    @extend .border-radius-3px;
                    background-color: $bg-body-field;
                }

                .content-text {
                    margin-top: 20px;
                }
            }

            .column-right {
                min-width: 760px;
                padding-left: 15px;
                
                .body-container-sport {
                    @extend .btn-bg-red;
                    @extend .border-radius-3px;
                }

                .card-content-sport {
                    border-bottom: 1px solid $border-right-cr;
                    padding-bottom: 10px;
                }
            }
        }
    }
</style>