<template>
    <div class="table-field">
        <!-- <amp-list width="auto" height="300px" layout="fixed-height" src="/data/tablelist.json" v-html="tableList" /> -->
        <amp-list class="table-responsive" id="myAmpList" reset-on-refresh layout="fixed-height" height="600" src="/data/tablelist.json" binding="no" v-html="tableList" />
    </div>
</template>

<script>
export default {
    data() {
        return {
            tableList: `
               <template type="amp-mustache">
                    <div class="product">
                        <div class="image-padding">
                            <amp-img width="50" height="50" alt="{{ name }}" src="{{ image }}"></amp-img>
                        </div>
                        <div>
                            <div class="font-size-name">{{ name }}</div>
                            <div class="font-size-price">{{ price }}</div>
                        </div>
                    </div>
                </template>
                `
        }
    },
}
</script>

<style lang="scss">
    .table-field {
        overflow: auto;
        height: 340px;
        background: $color-gray;
        border-bottom-left-radius: 5px;
        border-bottom-right-radius: 5px;
    }
    .table-field::-webkit-scrollbar {
            width: 5px;          
    }
    .table-field::-webkit-scrollbar-track {
        // background: $color-black;     
    }
    .table-field::-webkit-scrollbar-thumb {
        background-color: $color-white;    
        border-radius: 20px;       
        // border: 1px solid $color-white;  
    }
  .list-overflow {
    width: max-content;
    margin: var( --space-2);
    margin-left: auto;
    padding: var( --space-2);
    color: var(--color-text-light);
    background-color: var(--color-primary);
  }

  .product {
    // max-width: 400px;
    // box-shadow: var(--box-shadow-1);
    // background: var(--color-bg-light);
        border-radius: 2px;
        margin: 7px 25px;
        padding: 0px 0px 6px 10px;
        display: flex;
        align-items: center;
        border-bottom: 1px solid $color-white;
        .image-placeholder {
            margin-right: var(--space-3);
        }
        .image-placeholder {
            width: 150px;
            height: 100px;
            background-color: #999;
        }
        .image-padding {
            margin: 0px 50px 0px 0px;
        }
        .font-size-name {
            font-size: 15px;
            font-weight: 300;
        }
        .font-size-price {
            font-size: 30px;
            font-weight: 700;
            color: red;
            line-height: 32px;
            text-align: justify;
        }
        
  }
  amp-selector[role=tablist].tabs-with-flex [role=tabpanel][data-v-064377cf] {
            padding: 0px;
        }
//   amp-selector[role=tablist].tabs-with-flex [role=tab][selected] + [role=tabpanel][data-v-064377cf] {
//     overflow: auto;
//     position: relative;
//     max-height: 254px;
//   }

</style>