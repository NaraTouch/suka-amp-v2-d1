<template>
    <div class="tab-scroll-bar">
        <amp-selector class="tabs-with-flex scroll-bar" role="tablist" keyboard-select-mode="focus">
                <div id="tab1" role="tab" aria-controls="tabpanel1" option selected>WINNER</div>
                <div class="tab1-style" id="tabpanel1" role="tabpanel" aria-labelledby="tab1">
                    <table-field />
                </div>
                <div id="tab2" role="tab" aria-controls="tabpanel2" option>TOGEL</div>
                <div id="tabpanel2" role="tabpanel" aria-labelledby="tab2">Tab two content... </div>
                <div id="tab3" class="loading" role="tab" aria-controls="tabpanel3" option>DAILY WIN</div>
                <div id="tabpanel3" role="tabpanel" aria-labelledby="tab3">Tab three content... </div>
        </amp-selector>
    </div>
</template>

<script>
export default {
    components: {
        TableField: () => import('../Tab/TableField'),
    },
    data() {
        return {
            
        }
    },
}
</script>

<style lang="scss" amp-boilerplate>
    .tab-scroll-bar {
        overflow: auto;
        height: 385px;
        padding: 0px 11px 0px 0px;
        margin: 0px -18px 0px 0px;
        position: relative;

        &::-webkit-scrollbar-track {
            background-color: $scroll-bar-cr;
             border-radius: 2px;
        }

        &::-webkit-scrollbar {
            width: 6px;
        }

        &::-webkit-scrollbar-thumb {
            background-color: $scroll-cr;
            border-radius: 2px;
        }

        #tab3 { 
            
            border-top-right-radius: 4px;

        }
        .loading {
            &:after {
                display: block;
                content: "";
                position: absolute;
                top: -1px;
                right: 10px;
                background: url(/images/slider-promotion/hot-offer.png) no-repeat;
                background-size: contain;
                animation: blink 1.2s step-start 0s infinite;
                -webkit-animation: blink 1.2s step-start 0s infinite;
                padding: 12px;
            }
            @extend .keyframes;
        }

        amp-selector[role=tablist].tabs-with-flex {
            @extend .display-flex;
            @extend .font-size;
            flex-wrap: wrap;

            #tab1 {
                border-right: 1px solid $border-right-cr;
            }
            
            #tab2 {
                border-right: 1px solid $border-right-cr;
            }
        }

        amp-selector[role=tablist].tabs-with-flex [role=tab] {
            @extend .tab-bg-img;
            flex-grow: 1;
            text-align: center;
            color: $text-color-1;
            padding: 10px 8px 10px 5px;

            &:first-child {
                border-top-left-radius: 4px;
            }
        }

        amp-selector[role=tablist].tabs-with-flex [role=tab][selected] {
            @extend .tab-selec-bg-img;
            outline: none;
            color: white;
            padding: 10px;
        
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
            @extend .display-flex;
        }

        amp-selector[role=tablist].tabs-with-selector [role=tab][selected] {
            outline: none;
        }

        amp-selector[role=tablist].tabs-with-selector {
            @extend .display-flex;
        }

        amp-selector[role=tablist].tabs-with-selector [role=tab] {
        width: 100%;
        text-align: center;
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