<template>
  <div class="careers-wrapper" id="careers-openposition">
    <p>Drop your CV and a line at hr@edgistify.com</p>
    <h3>Let’s Make an Impact. Together!</h3>

    <v-container
      fluid
      class="bg-surface-variant"
      style="padding: 0; margin-top: 50px"
    >
      <v-row
        no-gutters
        v-for="index in 3"
        :key="index"
        class="careers-wrapper-row1"
        style="display: none"
      >
        <v-col lg="6" sm="12" cols="12" class="pr-6 pb-12">
          <div class="specialists-details">
            <div class="info-text">
              <h1>Role</h1>
              <div class="column">
                <div class="row1">
                  <img src="/career/experience-icon.png" contain />
                  <p>Experience</p>
                </div>

                <div class="row1">
                  <img src="/career/location-icon.png" contain />
                  <p>Location</p>
                </div>
              </div>
            </div>
            <div class="btn_container">
              <v-btn class="button bg-white">View Job Details</v-btn>
            </div>
          </div>
        </v-col>
        <v-col lg="6" sm="12" cols="12" class="pl-6 pb-12">
          <div class="specialists-details">
            <div class="info-text">
              <h1>Role</h1>
              <div class="column">
                <div class="row1">
                  <img src="/career/experience-icon.png" contain />
                  <p>Experience</p>
                </div>

                <div class="row1">
                  <img src="/career/location-icon.png" contain />
                  <p>Location</p>
                </div>
              </div>
            </div>
            <div class="btn_container">
              <v-btn class="button bg-white">View Job Details</v-btn>
            </div>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isSmallDevice: false,
    };
  },
  mounted() {
    if (window.innerWidth <= 850) {
      this.isSmallDevice = true;
    } else {
      this.isSmallDevice = false;
    }
  },
};
</script>

<style lang="scss" scoped>
@media (max-width: 850px) {
  .careers-wrapper {
    width: 100vw;
    height: auto !important;
    padding: 3% 0 0 0;
    background: #00a699;

    P {
      font-size: 12px !important;
      line-height: 15px !important;
    }

    h3 {
      width: 80% !important;
      padding-left: 5rem !important;
      font-size: 22px !important;
      line-height: 30px !important;
    }

    .para {
      font-family: "Outfit";
      font-style: normal;
      font-weight: 300;
      font-size: 16px;
      line-height: 20px;
      text-align: center;
      color: #ffffff;
    }

    .col-12 {
      padding: 0 !important;
    }

    .careers-wrapper-row1 {
      display: flex;
      justify-content: center;
      flex-direction: column !important;
      align-items: center;
      margin: 0 30px !important;

      .specialists-details {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        padding: 0px 0px !important;
        height: 62px !important;
        background: #ffffff;
        border-radius: 10px;
        margin: 0 !important;
        margin-bottom: 16px !important;
        color: black;
        width: auto !important;
        gap: 0 !important;

        .info-text {
          display: flex;
          flex-direction: column;
          align-items: start;
          padding: 0px;
          gap: 0 !important;
          height: auto !important;

          h1 {
            font-family: "Outfit" !important;
            font-style: normal !important;
            font-weight: 300 !important;
            font-size: 16.0164px !important;
            line-height: 20px !important;
            color: #313131 !important;
          }

          .column {
            display: flex;
            justify-content: flex-start;
            width: fit-content;

            .row1 {
              display: flex;
              justify-content: center;
              align-items: center;

              img {
                width: 38px;
                height: 38px;
              }

              p {
                font-family: "Outfit" !important;
                font-style: normal !important;
                font-weight: 300 !important;
                font-size: 8.00818px !important;
                line-height: 10px !important;
                color: #7a7a7a !important;
              }
            }
          }
        }

        .btn_container {
          display: flex;
          flex-direction: row;
          align-items: flex-start;
          gap: 10px;
          width: 87.03px !important;
          height: 21.01px !important;
          background: #00a699;
          border-radius: 35px;
          flex: none;

          .button {
            background: #00a699 !important;
            border-radius: 35px;
            width: 100% !important;
            height: 100% !important;
            font-family: "Noto Serif";
            font-style: normal;
            color: #ffffff;
            text-transform: capitalize;
            font-family: "Noto Serif" !important;
            font-size: 14px !important;
            line-height: 20px !important;
            font-weight: 300 !important;
          }
        }
      }
    }
  }
}

.careers-wrapper {
  width: 100vw;
  padding: 3% 0 0 0;
  background: #00a699;

  .btn_container {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    gap: 10px;
    width: 180px;
    background: #00a699;
    border-radius: 35px;
    flex: none;

    .button {
      background: #00a699;
      border-radius: 35px;
      width: 180px;
      height: 42px !important;
      font-family: "Noto Serif";
      font-style: normal;
      font-weight: 400;
      font-size: 13px;
      line-height: 22px;
      color: #ffffff;
      text-transform: capitalize;

      &.primary {
        background-color: #00a699;
        box-shadow: inset 0 0 0 0 #00a699;
        transition: color 0.3s ease-in-out, box-shadow 0.3s ease-in-out;

        &:hover {
          box-shadow: inset 230px 0 0 0 #000000;
          color: #ffffff;
        }
      }
    }
  }

  P {
    font-family: "Outfit";
    font-style: normal;
    font-weight: 300;
    font-size: 18px;
    line-height: 23px;
    text-align: center;
    color: #ffffff;
    margin: 12px;
  }

  h3 {
    font-family: "Noto Serif";
    font-style: normal;
    font-weight: 400;
    font-size: 35.4224px;
    line-height: 48px;
    text-align: center;
    color: #ffffff;
  }

  .para {
    font-family: "Outfit";
    font-style: normal;
    font-weight: 300;
    font-size: 16px;
    line-height: 20px;
    text-align: center;
    color: #ffffff;
  }

  .careers-wrapper-row1 {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 0 6%;

    .specialists-details {
      display: flex;
      flex-direction: row;
      justify-content: space-around;
      align-items: center;
      height: 123px;
      background: #ffffff;
      border-radius: 10px;
      color: black;
      margin-left: 4px;

      .info-text {
        display: flex;
        flex-direction: column;
        align-items: start;
        padding: 0px;
        gap: 20px;
        height: 100px;

        h1 {
          font-family: "Outfit";
          font-style: normal;
          font-weight: 300;
          font-size: 32px;
          line-height: 40px;
          padding-left: 0.5rem;
          color: #313131;
        }

        .column {
          display: flex;
          justify-content: flex-start;
          width: fit-content;

          .row1 {
            display: flex;
            justify-content: center;
            align-items: center;

            img {
              width: 38px;
              height: 38px;
            }

            p {
              font-family: "Outfit";
              font-style: normal;
              font-weight: 300;
              font-size: 16px;
              line-height: 20px;
              color: #7a7a7a;
              margin-left: 0px;
            }
          }
        }
      }
    }
  }
}
</style>
