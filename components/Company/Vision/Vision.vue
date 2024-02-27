<template>
  <div class="vision-conatiner" id="vision">
    <div class="vision-top">
      <p class="vision-top-title">What Sets Us Apart?</p>
      <div class="content-head">
        <h1>Consultative Approach</h1>
        <h1>Supply Chain Expertise</h1>
        <h1>Scalability and Flexibility</h1>
        <h1>Tech-enabled Operations</h1>
      </div>
    </div>
    <div></div>
    <v-col class="vision-bottom pb-0" md="12">
      <!-- <div class="vission-bottom-img">
            <v-img src="/Company/boxes-cropped-out.png" class="boxes-cropped-img"></v-img>
         </div> -->
      <v-img
        src="/Company/box.gif"
        cover
        class="bg-grey-lighten-2 image-gif"
      >
      </v-img>
      <div class="vission-bottom-wrapper">
        <h1>Vision</h1>
        <p>
          “We intend to help businesses grow with effective, effortless, and
          efficient supply chain management. As a team of experienced and
          techno-savvy supply chain professionals, we believe that technology is
          the future of the Indian supply chain and logistics industry. It is
          our aim to eliminate warehousing and fulfillment bottlenecks through
          simple, tech-driven and powerful solutions.”
        </p>
      </div>
      <!-- <div class="vision-bottom-img-wrapper">
            <v-img src="/Company/boxes.png" class="vision-bottom-box-img">

            </v-img>
         </div> -->
    </v-col>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
.vision-conatiner {
  .content-head {
    display: flex;
    margin-top: 20px;
    align-items: center;
    // justify-content: center;
    flex-direction: column;
    width: 100%;
    height: 200px;
    overflow: hidden;
    // border: 1px solid black;

    h1 {
      font-size: 120px;
      font-family: "Noto Serif";
      animation: infinite slide-top 15s linear;

      @keyframes slide-top {
        0% {
          transform: translateY(0%);
        }

        20% {
          transform: translateY(0%);
        }

        30% {
          transform: translateY(-100%);
        }

        40% {
          transform: translateY(-100%);
        }

        50% {
          transform: translateY(-200%);
        }

        70% {
          transform: translateY(-200%);
        }

        80% {
          transform: translateY(-300%);
        }

        90% {
          transform: translateY(-300%);
        }

        100% {
          transform: translateY(0%);
        }
      }
    }
  }

  .vision-top {
    width: 100%;
    height: 365px;
    background-color: #0c0c0c;
    text-align: center;
    //background-image: url('/Company/vision-background-grid.png');
    background-size: contain;
    background-position-x: right;

    .vision-top-title {
      font-family: "Noto Serif";
      padding-top: 48px;
      font-style: normal;
      font-weight: 500;
      font-size: 36px;
      line-height: 49px;
      color: #00a699;
    }

    h1 {
      font-family: "Noto Serif";
      font-style: normal;
      font-weight: 500;
      font-size: 87.7027px;
      line-height: 178.5%;
      color: #ffffff;
    }
  }
  .image-gif {
    width: 100vw;
  }

  .vision-bottom {
    background: #00a699;
    position: relative;

    .vission-bottom-wrapper {
      height: 100%;
      width: 40%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      position: absolute;
      top: 0;
      left: 30%;

      h1 {
        font-family: "Noto Serif";
        font-style: normal;
        font-weight: 500;
        font-size: 42px;
        line-height: 49px;
        color: #ffffff;
      }

      p {
        font-family: "Outfit";
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        line-height: 22px;
        color: #ffffff;
        margin-top: 2rem;
      }
    }

    .vision-bottom-img-wrapper {
      width: 100%;

      .vision-bottom-box-img {
        width: 79.38px;
        height: 134.81px;
        background-size: contain;
        top: 0px;
        left: 85rem;
      }
    }
  }
}

@media screen and (max-width: 1440px) and ( min-width: 850px) {
   .image-gif {
    width: 100vw;
    height: 420px !important;
  }
}

@media screen and (max-width: 850px) {

   .image-gif {
    width: 100vw;
    height: 9rem !important;
   }
  .vision-conatiner {
    width: 100%;
    height: auto !important;
    display: flex;
    flex-direction: column;

    .content-head {
      width: 100% !important;
      height: 40px !important;
      margin-top: 0 !important;
    }

    .vision-top {
      width: 100%;
      height: auto !important;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      background-color: #0c0c0c;
      padding: 6%;

      //background-image: url('/Company/vision-background-grid.png');
      background-size: contain;
      background-position-x: right;

      .vision-top-title {
        font-size: 1rem !important;
        line-height: 1.375rem !important;
        color: #00a699;
        padding-top: 0 !important;
        margin-bottom: 0 !important;
      }

      h1 {
        font-size: 1.375rem !important;
        line-height: 178.5% !important;
        color: #ffffff;
      }
    }

    .vision-bottom {
      width: 100%;
      height: auto !important;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      background: #00a699;
      position: relative;
      padding: 30% 0;

      .vission-bottom-img {
        position: absolute;
        left: 0px;
        top: 40% !important;

        .boxes-cropped-img {
          width: 10px;
        }
      }

      .vission-bottom-wrapper {
        height: 100%;
        width: 80% !important;
        display: flex;
        flex-direction: column;
        justify-content: baseline;
        align-items: center;
        margin-top: 1rem;
        left: 50px !important;

        h1 {
          font-size: 30px !important;
          line-height: 0.063rem !important;
        }

        p {
          font-family: "Outfit" !important;
          font-style: normal;
          font-weight: 400;
          font-size: 16px !important;
          line-height: 20px !important;
          color: #ffffff;
          margin-top: 2rem;
        }
      }

      .vision-bottom-img-wrapper {
        width: 100%;
        padding-top: 6% !important;

        .vision-bottom-box-img {
          width: 5% !important;
          height: 3% !important;
          left: 86% !important;
        }
      }
    }
  }
}
</style>
