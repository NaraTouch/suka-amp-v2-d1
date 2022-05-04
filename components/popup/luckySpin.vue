<template>
    <div class="modal_boxs">
       <div class="header-image">
           <div class="image-pr">
                <amp-img alt="lucky-spin" src="/images/popup/lucky-spin-image.png" width="575" height="530" />
            </div>
            <div class="btn-style">
                <button class="btn">Main Sekarang</button>
            </div>
       </div>

       <div class="body-title">
            <h5><strong>SELAMAT DATANG DI SUKAPOIN REWARD SUKABET</strong></h5>
            <div>
                <ol>
                    <h5 class="h3-mr"><strong>Pragmatic Play Slot</strong></h5>
                    <li><p>Sukabet adalah agen bola casino online terpercaya di nidonesia sejak tahun 2010 ,kini hadir dengan sistem terbaru yaitu point REWARD.</p></li>
                    <li><p>Log in dan klik tombol spin di sukabet setiap hari ,maka anda akan mendapatkun poin secara cuman-cuma tanpa syarat.</p></li>
                    <li><p>Ada 2 cara untuk mendapatkan point reward yaitu turnover dan free spin </p></li>
                        <ol class="dashed"> 
                        <li><p>untuk turnover bisa di dapatkan dengan bermain bola, casino, slot yang ada di sukabet.</p></li>
                        <li><p>untuk free spin bisa di dapatkan setiap hari dari jam 00:00 - 23:59 setlah log in sukabet</p></li>
                    </ol>
                </ol>
                
                <ol>   
                    <h5 class="h3-mr"><strong>TURNOVER</strong></h5> 
                    <li><p>Member dengan id bms-1 bermain bola dalam 1 hari mencapai turnover 10.000.000 maka 10.000.000 / 3.888.000 = 2.57 poin</p></li>
                    <li><p>Member dengan id bms-1 bermain casino dalam 1 hari mencapai turnover 10.000.000 maka 10.000.000 / 6.888.000 = 1.45 poin</p></li>
                    <li><p>Member dengan id bms-1 bermain slot dalam 1 hari mencapai turnover 10.000.000 maka 10.000.000 / 8.888.000 = 1.12 poin</p></li>
                    <li><p>Poin dari turnover ini selalu di akumulasi dari 3 jenis game di atas selama member masih aktif bermain</p></li>
                </ol>
                
                <ol>
                    <h5 class="h3-mr"><strong>FREE SPIN</strong></h5>
                    <li><p>Member log in di sukabet antara jam 00:00 - 23:59 akan mendapatkan spin cuma cuma 1x dan bisa spin lagi di hari esok nya. setiap hari.</p></li>
                    <li><p>Member melakulan spin dan dapet 1.000.000 maka 1.000.000 / 100.000 = 10 poin</p></li>
                    <li><p>Poin dari free spin ini selalu di akumulasi setiap hari blia member melakukan free spin setiap hari.</p></li>
                </ol>
            </div>
       </div>
    </div>
</template>

<script >
    export default {
        components: {
            
        }
    }

    
</script>
        
<style lang="scss" amp-boilerplate>
    .modal_boxs {
        width: 600px;
        @extend .magrin-0-auto;
        background: #38383c;
        padding: 10px;
        border-radius: 6px;

        .header-image {
            .image-pr {
                    padding: 0px 0px 0px 2px;
            }

            .btn-style {
                display: block;
                position: absolute;
                margin: -50px 0px 0px 0px;
                left: 0;
                right: 0;
                text-align: center;

                .btn {
                    @extend .btn-custom;
                    @extend .btn-bg-red;
                    @extend .color-white;
                    cursor: pointer;
                    padding: 7px 30px 7px 30px;
                }
            }
        } 
        
        .body-title {
            background: #414145;
            padding: 10px;
            margin: 10px 5px 0px 5px;
            border-radius: 6px;
            color: $color-white;

            
            ol {
                padding: 0px 0px 0px 15px;

                .h3-mr {
                    margin: 0px -15px;
                }

                li {
                    font-size: 12px;
                }

                .dashed {
                    list-style-type: none;
                    padding-left: 1em;

                    li {
                        font-size: 12px;

                        &:before {
                            content: "-";
                            position: absolute;
                            margin-left: -12px;
                        }
                    }
                }
            }
        }
    }
</style>