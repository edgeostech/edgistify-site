<template>
  <v-container fluid class="founders-container">
    <h1 class="title">Meet Our Founders</h1>
    <v-row class="founders-main" no-gutters justify="space-between">
      <v-col sm="12" md="4" class="scm-wrapper-row1 px-md-6 pb-6" cols="12">
        <div class="img1-div">
          <v-img
            src="/Company/founder-edgistify-kamal-kumawat.jpg.jpg"
            class="founders-img"
          ></v-img>
          <h1>Kamal Kumawat</h1>
          <p>Co-founder and Director</p>
          <p class="para">IIT Bombay Alumni</p>
        </div>
      </v-col>
      <v-col sm="12" md="4" class="scm-wrapper-row1 px-md-6 pb-6" cols="12">
        <div class="img1-div">
          <v-img
            src="/Company/founder-edgistify-antim-suman.jpg.jpg"
            class="founders-img"
          ></v-img>
          <h1>Antim Suman</h1>
          <p>Co-founder and Director</p>
          <p class="para">NIT Surat Alumni</p>
        </div>
      </v-col>
      <v-col sm="12" md="4" class="scm-wrapper-row1 px-md-6 pb-6" cols="12">
        <div class="img1-div">
          <v-img
            src="/Company/founder-edgistify-umang-shukla.jpg.jpg"
            class="founders-img"
          ></v-img>
          <h1>Umang Shukla</h1>
          <p>Co-founder and Director</p>
          <p class="para">IIT Kanpur Alumni</p>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup></script>

<style lang="scss" scoped>
.scm-wrapper-row1:first-child {
  margin-left: -24px;
}
.scm-wrapper-row1:last-child {
  margin-right: -24px;
}
p {
  margin-bottom: 0.25rem !important;
}
.founders-container {
  width: 100%;
  background: #ffff;
  padding: 0 6% !important;
  margin-bottom: 2%;

  .title {
    font-family: "Noto Serif" !important;
    font-style: normal;
    font-weight: 500;
    font-size: 42px !important;
    line-height: 47px;
    padding-top: 36px;
    padding-bottom: 30px;
    color: #1a1a1a;
  }

  .founders-main {
    width: 100%;
    display: flex;
    // padding-left: 5rem;
    justify-content: space-between;

    .img1-div {
      height: 100%;
      .founders-img {
        margin-bottom: 10px;
      }

      h1 {
        font-family: "Outfit";
        font-style: normal;
        font-weight: 500;
        font-size: 16px;
        line-height: 20px;
        color: #1a1a1a;
      }

      p {
        font-family: "Outfit";
        font-style: normal;
        font-weight: 300;
        font-size: 14px;
        line-height: 18px;
        color: #1a1a1a;
      }

      .para {
        font-size: 12px;
        line-height: 15px;
      }
    }
  }
}

@media screen and (max-width: 850px) {
  .scm-wrapper-row1:first-child {
    margin-left: 0;
  }
  .scm-wrapper-row1:last-child {
    margin-right: 0;
  }
  .founders-container {
    width: 100%;
    height: auto !important;
    background: #ffff;
    padding: 0 30px !important;

    .title {
      font-family: "Noto Serif";
      font-style: normal;
      font-weight: 500;
      font-size: 30px !important;
      line-height: 2.063rem !important;
      color: #1a1a1a;
    }
    .col {
      padding-right: 0 !important;
      padding-bottom: 8px !important;
    }

    .founders-main {
      width: 100% !important;
      flex-direction: column !important;
      align-items: center !important;

      .img1-div {
        width: 100% !important;

        h1 {
          font-size: 16px !important;
        }

        p {
          font-size: 14px;
        }

        .para {
          font-size: 14px;
        }
      }
    }
  }
}
</style>
