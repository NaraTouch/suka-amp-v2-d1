<template>
    <div class="table-field">
        <amp-list class="table-responsive" id="myAmpList" reset-on-refresh layout="fixed-height" height="725" src="/data/table-field-list-winner.json" binding="no" v-html="tableList" />
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
                            <amp-img width="60" height="60" alt="{{ name }}" src="{{ image }}"></amp-img>
                        </div>
                        <div class="tab-text">
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

<style lang="scss" amp-boilerplate>
    .table-field {
        background: $bg-body-field;
        @extend .br-bottom-right-left;

        .list-overflow {
            width: max-content;
            margin-left: auto;
           
        }

        .product {
            @extend .display-flex;
            margin: 7px 15px;
            padding: 0px 0px 0px 10px;
            align-items: center;
            border-bottom: 1px solid $border-right-cr;


            .image-placeholder {
                width: 150px;
                height: 100px;
                background-color: #999;
            }

            .image-padding {
                margin: 0px 25px 0px 0px;
            }

            .tab-text {
                margin: 5px;

                .font-size-name {
                    font-size: 13px;
                    font-weight: 200;
                    color: $tab-cr;
                    margin: 0px 0px 5px 1px;
                }

                .font-size-price {
                    font-size: 45px;
                    font-weight: 700;
                    color: $text-red;
                    line-height: 32px;
                    text-align: justify;
                }
            }
        }
        
        amp-selector[role=tablist].tabs-with-flex [role=tabpanel][data-v-064377cf] {
            padding: 0px;
        }
    }
</style>