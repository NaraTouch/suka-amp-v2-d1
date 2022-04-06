<template>
    <div class="testss">
        <amp-selector class="tabs-with-flex" role="tablist" keyboard-select-mode="focus">
            <div id="tab1" role="tab" aria-controls="tabpanel1" option selected>Winner</div>
            <div class="tab1-style" id="tabpanel1" role="tabpanel" aria-labelledby="tab1">
                <table-field />
            </div>
            <div id="tab2" role="tab" aria-controls="tabpanel2" option>ToGel</div>
            <div id="tabpanel2" role="tabpanel" aria-labelledby="tab2">Tab two content... </div>
            <div id="tab3" role="tab" aria-controls="tabpanel3" option>Daily Win</div>
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

<style lang="scss" > 
    .tab1-style {
        // height: 350px;
    } 
    // .testss {
    //     display: grid;
    // }
    // border-radius 
    #tab3 {
        border-top-right-radius: 5px;
    }
    amp-selector[role=tablist].tabs-with-flex {
        display: flex;
        flex-wrap: wrap;
        // padding: 1px;
    }
    amp-selector[role=tablist].tabs-with-flex [role=tab] {
        flex-grow: 1;
        text-align: center;
        padding: var(--space-1);
        background: $color-gray;
        color: $text-color-1;
        padding: 10px;
        
        &:first-child {
             border-top-left-radius: 5px;
        }
        
    }
    amp-selector[role=tablist].tabs-with-flex [role=tab][selected] {
        outline: none;
        // border-bottom: 2px solid var(--color-primary);
        background: $btn-color-1;
        color: white;
        padding: 10px;
       
    }
    amp-selector[role=tablist].tabs-with-flex [role=tabpanel] {
        display: none;
        width: 100%;
        order: 1; 
        // padding: var(--space-4);
    }
    amp-selector[role=tablist].tabs-with-flex [role=tab][selected] + [role=tabpanel] {
        display: block;
    }

    amp-selector[role=tablist].tabs-with-selector {
        display: flex;
    }
    amp-selector[role=tablist].tabs-with-selector [role=tab][selected] {
        outline: none;
        border-bottom: 2px solid var(--color-primary);
    }
    amp-selector[role=tablist].tabs-with-selector {
        display: flex;
    }
    amp-selector[role=tablist].tabs-with-selector [role=tab] {
      width: 100%;
      text-align: center;
      padding: var(--space-1);
    }
    amp-selector.tabpanels [role=tabpanel] {
      display: none;
      padding: var(--space-4);
    }
    amp-selector.tabpanels [role=tabpanel][selected] {
      outline: none;
      display: block;
    }

</style>