<template>
  <v-container fluid class="our-message-container">
    <v-row no-gutters class="top image-container" style="margin-left: -3%">
      <v-img src="/Homepage/OurMessage/top.png" class="img" contain />
    </v-row>
    <v-col class="content-container">
      <div class="content-head">
        <h1 class="mob">Design</h1>
        <h1 class="mob">Execute</h1>
        <h1 class="mob">Optimize</h1>
        <h1 class="mob">Design</h1>
      </div>
      <span>Your Supply Chain</span>
    </v-col>
    <v-row no-gutters class="bottom image-container" style="margin-right: -5%">
      <v-img src="/Homepage/OurMessage/bottom.png" class="img" contain />
    </v-row>
  </v-container>
</template>

<style lang="scss" scoped>
.our-message-container {
  display: flex;
  width: 100%;
  height: 26.25rem;
  background-color: white;
  align-items: center;
  justify-content: center;

  .backgroung-img {
    position: absolute;
    width: 100%;
    height: 420px;
    display: block;
    left: -85px;
  }

  .image-container {
    display: flex;
    width: 22.5%;
    height: 100%;

    &.top {
      align-items: flex-start;

      .img {
        margin: -2% 0 0 -20%;
        height: 14.563rem;
      }
    }

    &.bottom {
      align-items: flex-end;
      justify-content: flex-end;

      .img {
        margin: 0 -20% -2% 0;
        height: 215px;
      }
    }
  }

  .content-container {
    display: flex;
    // width: 55%;
    flex-direction: column;
    align-items: center;
    height: 75%;
    position: relative;

    .content-head {
      display: flex;
      align-items: center;
      // justify-content: center;
      flex-direction: column;
      // width: 100%;
      height: auto;
      overflow: hidden;
      // border: 1px solid black;

      h1 {
        font-size: 7.5rem;
        font-family: "Noto Serif";
        animation: infinite slide-top 15s linear;
        color: #00a699;

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

          50% {
            transform: translateY(-100%);
          }

          60% {
            transform: translateY(-200%);
          }

          80% {
            transform: translateY(-200%);
          }

          90% {
            transform: translateY(-300%);
          }

          100% {
            transform: translateY(-300%);
          }
        }
      }
    }

    span {
      font-size: 2rem;
      line-height: 57px;
      font-weight: 300;
      color: #00a699;
      font-family: 'Outfit';
    }

  }


}

@media (max-width: 850px) {


  .our-message-container {
    display: flex !important;
    width: 100% !important;
    height: auto !important;

    // .backgroung-img {
    //   height: 196px !important;
    //   left: 10px !important;
    // }

    .image-container {
      display: flex !important;
      // width: 25% !important;
      height: 100% !important;

      &.top {
        align-items: flex-start !important;

        .img {
          margin: -70% 0 0 -20% !important;
          height: auto !important;
        }
      }

      &.bottom {
        align-items: flex-end !important;
        justify-content: flex-end !important;

        .img {
          margin: 20px 0% -50% 0 !important;
          height: auto !important;
        }
      }
    }

    .content-container {
      height: auto !important;

      .content-head {
        height: 3.125rem !important;
        overflow: hidden !important;
        align-items: center !important;
        align-content: center !important;

        h1 {
          font-size: 2.188rem !important;
          font-weight: 500 !important;
          align-items: center !important;
          align-content: center !important;
          // animation: infinite slide-top 15s linear !important;

          // @keyframes slide-top {
          //   0% {
          //     transform: translateY(0%) !important;
          //   }

          //   20% {
          //     transform: translateY(0%) !important;
          //   }

          //   30% {
          //     transform: translateY(-100%) !important;
          //   }

          //   50% {
          //     transform: translateY(-100%) !important;
          //   }

          //   60% {
          //     transform: translateY(-200%) !important;
          //   }

          //   80% {
          //     transform: translateY(-200%) !important;
          //   }

          //   90% {
          //     transform: translateY(-300%) !important;
          //   }

          //   100% {
          //     transform: translateY(-300%) !important;
          //   }
          // }
        }
      }

      span {
        font-size: 1rem !important;
      }
    }
  }
}
</style>

<script>
import aosMixin from "~/mixins/aos";

export default {
  mixins: [aosMixin],
};
</script>
