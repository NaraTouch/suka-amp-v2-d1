<template>
    <div class="modal_box">
        <div class="modal-header">
            <div class="header-title image-header">
                <span>Registration</span>
            </div>

            <div class="header-close">
                <button class="done_modalbox btn-style" on="tap:modalbox.close" role="button" tabindex="0" title="Tamam">X</button>
            </div>
        </div>

        <div class="modal-body">
            <form class="d-register-form" method="post" action-xhr="/documentation/examples/api/submit-form-input-text-xhr" target="_top">
                <div class="body-left">
                    <label>
                        <p>Login ID<span class="red">*</span></p>
                        <input type="text" name="name" placeholder="Login ID.." required>
                    </label>
                    <br>
                    <label>
                        <p>Password<span class="red">*</span></p>
                        <input type="password" name="email" placeholder="Password.." required>
                    </label>
                    <br>
                     <label>
                        <p>Konfirmasi Password<span class="red">*</span></p>
                        <input type="text" name="name" placeholder="Konfirmasi Password..." required>
                    </label>
                    <br>
                    <label>
                        <p>Bank<span class="red">*</span></p>
                        <select name="color" id="color" on="change:AMP.setState({ optionValue: true })" required>
                            <option value="" disabled selected >Pilih Bank</option>
                            <option value="BANK BRI">BRI BANK</option>
                            <option value="red">CIMA BANK</option>
                            <option value="green">MANDIRI BANK</option>
                            <option value="red">DANAMON BANK</option>
                            <option value="green">BCA BANK</option>
                            <option value="red">BNI BANK</option>
                            <option value="green">PERMATA BANK</option>
                            <option value="red">PANIN BANK</option>
                        </select>
                    </label>
                    <br>
                    <label>
                        <p>Nama di Rekening<span class="red">*</span></p>
                        <input type="text" name="email" placeholder="Nama di Rekening..." required>
                    </label>
                    <br>
                    <label>
                        <p>Nomor Rekening<span class="red">*</span></p>
                        <input type="text" name="email" placeholder="Nomor Rekening..." required>
                    </label>
                </div>

                <div class="body-right">
                     <label>
                        <p>Nomor Telepon<span class="red">*</span></p>
                        <input type="text" name="name" placeholder="Nomor Rekening..." required>
                    </label>
                    <br>
                    <label>
                        <p>Referal<span class="red">*</span></p>
                        <input type="text" name="email" placeholder="Referal..." required>
                    </label>
                    <label class="code-style">
                        <p>Kode Validasi<span class="red">*</span></p>
                        <div class="code-row">
                            <div>
                                <input class="code-input" style="width: 220px;" type="text" name="email" placeholder="code..." required>
                            </div>
                            <div class="span-style-code">
                                <span class="span-style">1234</span>
                            </div>
                        </div>
                    </label>
                    <br>
                    <label>
                        <div class="checkbox-row">
                            <div>
                                <input type="checkbox" style="width: 17px; height: 17px;" id="vehicle1" name="vehicle1" value="Bike">
                            </div>

                            <div class="checkbox-text">
                                <span>Saya sudah berusia lebih dari 18 tahun dan sudah membaca dan menerimu Syarat & Ketenuan, Kebijakan peraturn untuk bertaruh seperit yang tertulis di situs ini.</span>
                                <div class="checkbox-span-style">
                                    <span>Semun data yang anda isi di form pendaftaran ini di jamin kernhasiaannya 100%</span>
                                </div>
                            </div>
                        </div>
                    </label>

                    <div class="btn-style">
                        <button class="btn">Daftar</button>
                    </div>
                </div>
            </form>
        </div>
        
        <div class="modal-footer">
            <footers :hide="hide" />
        </div>
    </div>
    </template>
</template>

<script>
    export default {
        components: { 
            Footers: () => import('../Footers')
        },
        data() {
            return {
                image: '/images/card/hot-game-image.png',
                hide: false,
            }
        },
    }
</script>

<style lang="scss" amp-boilerplate>
    .modal_box {
        width: 900px;
        @extend .magrin-0-auto;
        
        .modal-header {
            display: grid;
            grid-template-columns: 1fr 40px;
            background-color: #292d39;
            border-top-right-radius: 7px;
            border-top-left-radius: 7px;
            .header-title {
                margin: 10px 0px 10px 80px;
                span {
                    font-size: 30px;
                    font-weight: bold;
                    color: $color-white;
                }
            }

            .header-close {
                margin: 5px 0px;
                .btn-style {
                    border: 0;
                    background: transparent;
                    color: $color-white;
                    font-size: 25px;
                    font-weight: bold;
                    cursor: pointer;
                }
            }

            .image-header {
                &:after {
                   display: block;
                    content: "";
                    position: absolute;
                    margin: -35px 0px 0px -60px;
                    padding: 32px;
                    background: url(/images/card/hot-game-image.png) no-repeat;
                    background-size: contain;
                }
            }
        }
       
        .modal-body {
            .d-register-form {
                @extend .display-grid;
               grid-template-columns: 1fr 1fr;
               margin: 10px 10px;
                .body-right {
                    .btn-style {
                        float: right;
                        margin: 50px 0px 0px 0px;
                       
                        .btn {
                            @extend .btn-bg-red;
                            @extend .border-radius-3px;
                            padding: 15px 30px 15px 30px;
                            font-weight: 700;
                            color: $color-white;
                            border: 1px;
                            font-size: 20px;
                            cursor: pointer;
                        }
                   }
                }
            } 

             .code-style {
                display: grid;
            }

           
            label {
                select:required:invalid {
                    color: #666;
                }
                option[value=""][disabled] {
                    display: none;
                }
                option {
                    color: #000;
                }

                .red {
                    color: $text-red;
                }
                .code-row {
                    @extend .display-grid;
                    grid-template-columns: 1fr 1fr;
                    .span-style-code {
                        display: inline-block;
                        margin: 8px 0px 0px 0px;
                        .span-style {
                            background: $text-red;
                            padding: 0px 10px;
                            border-radius: 3px;
                            font-size: 36px;
                            font-weight: bold;
                        }
                    }
                }

                .checkbox-row {
                    display: flex;
                    .checkbox-text {
                        margin-left: 10px;
                        .checkbox-span-style {
                            margin: 10px 0px 0px 0px;
                            span {
                                font-weight: bold;
                            }
                        }
                    }
                }

                input[type=text], select, input[type=password] {
                    @extend .border-radius-3px;
                    width: 100%;
                    padding: 12px 20px;
                    margin: 8px 0;
                    display: inline-block;
                    border: 1px solid #ccc;
                    box-sizing: border-box;
                }

                input[type=submit] {
                    width: 100%;
                    color: $color-white;
                    padding: 14px 20px;
                    margin: 8px 0;
                    border: none;
                    border-radius: 4px;
                    cursor: pointer;
                }
            }
        }

        .modal-footer {
            background-color: #292d39;
            padding: 15px 10px;
            border-bottom-right-radius: 7px;
            border-bottom-left-radius: 7px;
        }
    }
</style>