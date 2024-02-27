<template>
  <v-container fluid class="supportservices-benefits-main">
    <v-row
      class="careers-wrapper-row1 py-6 py-md-12"
      no-gutters
      justify="space-between"
    >
      <v-col cols="6" sm="6" md="4" class="pr-3 pb-6 pr-md-6 pb-md-6">
        <div class="specialists-details">
          <v-img src="/Solutions/supportservices/imag1.png" class="img"></v-img>
          <div class="info-text">
            <p>Fire Control</p>
          </div>
        </div>
      </v-col>
      <v-col cols="6" sm="6" md="4" class="pl-3 pb-6 px-md-6 pb-md-6">
        <div class="specialists-details">
          <v-img src="/Solutions/supportservices/imag2.png" class="img"></v-img>
          <div class="info-text">
            <p>CCTV Monitoring</p>
          </div>
        </div>
      </v-col>
      <v-col cols="6" sm="6" md="4" class="pl-md-6 pl-0 pr-3 pb-6 pr-md-0">
        <div class="specialists-details">
          <v-img src="/Solutions/supportservices/imag3.png" class="img"></v-img>
          <div class="info-text">
            <p>24/7 Security</p>
          </div>
        </div>
      </v-col>
      <v-col cols="6" sm="6" md="4" class="pl-3 pr-md-6 pl-md-0 py-md-6 pb-6">
        <div class="specialists-details">
          <v-img src="/Solutions/supportservices/imag4.png" class="img"></v-img>
          <div class="info-text">
            <p>Biometric System Access</p>
          </div>
        </div>
      </v-col>
      <v-col cols="6" sm="6" md="4" class="px-md-6 py-md-6 pr-3">
        <div class="specialists-details">
          <v-img src="/Solutions/supportservices/imag5.png" class="img"></v-img>
          <div class="info-text">
            <p>Pest Control</p>
          </div>
        </div>
      </v-col>
      <v-col cols="6" sm="6" md="4" class="pl-md-6 py-md-6 pl-3 ">
        <div class="specialists-details">
          <v-img src="/Solutions/supportservices/imag6.png" class="img"></v-img>
          <div class="info-text">
            <p>Barcode Tracking System</p>
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup></script>

<style lang="scss" scoped>


.supportservices-benefits-main {
  background: #fdfdfd;
  padding: 0 6%;

  .careers-wrapper-row1 {
    .specialists-details {
      background: #f3f3f5;
      padding: 40px 20px;

      .img {
        width: 3.813rem;
        margin-bottom: 0.5rem;
        margin: auto;
      }

      .info-text {
        margin: 1.5rem 0 0 0;
        display: flex;
        justify-content: center;

        p {
          font-family: "Outfit";
          font-style: normal;
          font-weight: 400;
          font-size: 16px;
          line-height: 20px;
          text-align: center;
          color: #000000;
        }
      }
    }
  }
}

@media (max-width: 850px) {
  .specialists-details {

    height: 200px;

  }}
</style>
