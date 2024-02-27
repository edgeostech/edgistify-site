<template>
    <div class="contact-us-container">
        <div class="container-left">
            <div class="container-title">
                <h1>
                    Contact Us
                </h1>
            </div>
            <div class="container-quote">
                <h2>
                    Have questions about the Edgistify Logistics Programs? <br>
                    Please give us a call or email the address below.
                </h2>
            </div>

            <div class="container-address">
                <P>
                    Office line: +91-7505050505 <br>
                    Email: info@edgistify.com <br>
                    For all press and media inquiries, please email <br>
                    business@edgistify.com
                </P>
                
            </div>

        </div>

        <div class="container_right">
            <div class="img-div">
                <v-img src="/contact/office.png" class="img"></v-img>
            </div>
        </div>
    </div>

</template>

<style lang="scss" scoped>
@media (max-width: 800px) {
    .contact-us-container{
        flex-wrap: wrap !important;
        height: auto !important;
        flex-direction: column-reverse !important;
        .container-left , .container_right{
            width: 100% !important;
        }
        .img-div {
            position: relative !important;
            margin: 0 !important;
        }
    }
}
.contact-us-container{
    display: flex;
    width: 100%;
    height: 732px;
    background-color: #fff;
    .container-left{
        display: flex;
        flex-direction: column;
        width: 45%;
        height: 100%;
        // background-color: #fff;
        padding: 12% 25px 10% 6.82%;
        color: #000000;
        .container-title{
            display: flex;
            position: relative;
            // width: 225px;
            // height: 63px;
            // padding-left: 92px;
          
            h1 {
                font-family: 'Noto Serif';
                font-style: normal;
                font-weight: 300;
                font-size: 46.61px;
                line-height: 63px;
                // color: #000000;
            }
        }
        .container-quote{
            // width: 390px;
            // height: 40px;
            // padding-left: 92px;
            padding-top: 5%;
            display: flex;
            position: relative;
            h2 {
                font-family: 'Outfit';
                font-style: normal;
                font-weight: 300;
                font-size: 16px;
                line-height: 20px;
                // color: #000000;
            }
        }
        .container-address {
            padding-top: 5%;
            display: flex;
            position: relative;
        }
        P {
            font-family: 'Outfit';
            font-style: normal;
            font-weight: 300;
            font-size: 16px;
            line-height: 20px;
        }
    }
    .container_right{
        display: block;
        position: relative;
        width: 55%;
        height: 100%;
        padding: 0 0 0 0;
        .img-div{
            // align-items: center;
            position: absolute;
            height: 100%;
            width: 100%;
            object-fit: cover;
            object-position: right;
            margin-top: 9%;
            margin-bottom: 9%;
        }
    }
}
</style>

<script setup></script>
