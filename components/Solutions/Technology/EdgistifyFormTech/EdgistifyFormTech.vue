<template>
  <v-container fluid class="form-main">
    <v-row no-gutters class="main-left pa-0 pa-md-10">
      <h1>
        Schedule a Demo to
        See Our Dashboard
        Up Close
      </h1>
    </v-row>
    <v-row no-gutters class="main-right pa-0">
      <v-col class="right-name">
        <v-col class="form-row px-0 px-md-10">
          <v-col class="field-container px-0 px-md-10">
            <label class="field-lbl">Name *</label>
            <input type="text" id="name" name="name" class="name_field" required />
          </v-col>
          <v-col class="field-container px-0 px-md-10">
            <label class="field-lbl">Company/Organization *</label>
            <input type="text" id="name" name="name" class="name_field" required />
          </v-col>
        </v-col>
        <v-col class="form-row px-0 px-md-10">
          <v-col class="field-container px-0 px-md-10">
            <label class="field-lbl">Email *</label>
            <input type="text" id="name" name="name" class="name_field" required />
          </v-col>
          <v-col class="other-container px-0">
            <label class="field-lbl-othr">Phone number *</label>
            <v-col class="mobile-wrapper px-0">
              <select name="mobile" id="mobile" class="dropdown">
                <option value="india">+91</option>
              </select>
              <input type="text" id="name" name="name" class="name_field-othr" required />
            </v-col>
          </v-col>
        </v-col>
        <v-col class="form-row-last px-0 px-md-10">
          <div class="btn-container">
            <v-btn class="button btn" data-aos="fade-up" data-aos-once="true" data-aos-easing="ease-in"
              data-aos-duration="1000">Submit</v-btn>
          </div>
        </v-col>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
      isSmallDevice: false,
    };
  },
  mounted () {
    if (window.innerWidth <= 850) {
      this.isSmallDevice = true;
    } else {
      this.isSmallDevice = false;
    }
  },
};
</script>

<style lang="scss" scoped>
.form-main {
  width: 100%;
  display: flex;
  background: #00A699;

  .main-left {
    width: 30%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    height: auto;
    // padding: 6% 0 6% 6%;
    // margin-left: 6rem;

    h1 {
      padding: 0 4% 25% 6%;
      font-family: "Noto Serif";
      font-style: normal;
      font-weight: 400;
      font-size: 40px;
      line-height: 54px;
      // margin: 1 0 0 4rem;
      color: #ffffff;
    }

    p {
      font-family: "Outfit";
      font-style: normal;
      font-weight: 300;
      font-size: 16px;
      line-height: 20.16px;
      // margin: 1 0 0 4rem;
      // padding-top: 8%;
      // padding-bottom: 25%;
      color: #ffffff;
    }
  }

  .main-right {
    width: 70%;
    height: auto;
    display: flex;


    // padding: 0 1% 0 1%;

    .right-name {
      width: 100%;
      // height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 6% 6% 6% 0;
      // margin: 1rem 0 0 0;

      .form-row {
        width: 100%;
        display: flex;
        // flex-direction: column;
        align-items: center;
        justify-content: center;
        // margin: 1rem;

        .field-container {
          display: flex;
          flex-direction: column;
          // margin: 1.5rem;

          .name_field {
            box-sizing: border-box;

            width: 20.5rem;
            height: auto;

            background: #00A699;
            border-bottom: 1px solid #ffffff;
          }

          .name_field:focus {
            outline: none;
            caret-color: #ffffff;
          }

          .field-lbl {
            font-family: "Outfit";
            font-style: normal;
            font-weight: 400;
            font-size: 16px;
            line-height: 20px;
            color: #ffffff;
          }

          .field-container {
            // width: 156px;
            height: auto;
            // left: 1192px;
            // top: 379px;
            background: #ffffff;
            border-radius: 44px;
          }
        }

        .other-container {
          display: flex;
          flex-direction: column;
          // margin: 1.5rem;

          .field-lbl-othr {
            font-family: "Outfit";
            font-style: normal;
            font-weight: 400;
            font-size: 16px;
            line-height: 20px;
            color: #ffffff;
          }

          .mobile-wrapper {
            width: 80%;
            // margin: 0 0.5rem 0 0;
            display: flex;
            justify-content: space-between;

            .dropdown {
              width: 5.5rem;
              outline: none;
              // text-align: center;
              padding-left: 1.5rem;
              display: flex;
              color: #ffffff;
              background-image: url("/Solutions/warehousing/down-arrow.png");
              // background-size: cover;
              background-position-y: center;
              background-position-x: 4rem;
              background-color: transparent;
              border-bottom: 1px solid #ffffff;
            }

            .name_field-othr {
              box-sizing: border-box;
              width: 13rem;
              height: auto;
              background: #00A699;
              margin-left: 20px;
              border-bottom: 1px solid #ffffff;
            }

            .name_field-othr:focus {
              outline: none;
              caret-color: #ffffff;
            }
          }
        }
      }

      .form-row-last {
        width: 100%;
        display: flex;
        justify-content: end;
        margin-right: 17%;
        // margin: 1rem 30rem 0 3rem;


        .btn-container {
          display: flex;
          // width: 156px;
          height: auto;
          // margin: 2rem 0rem 0 0;
          // padding-left: 2rem;

          .button {
            // width: 100%;
            font-style: normal;
            font-weight: 600;
            line-height: 20px;
            color: #00A699 !important;
            background-color: #ffffff !important;
            border-radius: 44px;
            font-family: "Noto Serif";
            font-size: 16px;
            // margin: 0 0 0 10.5rem;
            text-transform: unset !important;
            border: none;
            letter-spacing: 0px;
          }
        }
      }
    }
  }
}

@media (max-width: 850px) {
  .form-main {
    display: flex !important;
    flex-direction: row !important;
    flex-wrap: wrap !important;
    width: 100% !important;
    height: auto !important;
    padding: 6%;

    .main-left {
      width: 100% !important;
      height: auto !important;
      // margin: 1rem !important;

      h1 {
        padding: 0 !important;
        font-size: 1.5rem !important;
        line-height: 2rem !important;
      }
    }

    .main-right {
      // display: flex;
      // flex-direction: row;
      height: auto !important;
      // flex-wrap: wrap;
      // width: 100%;

      .right-name {
        display: flex !important;
        flex-direction: row !important;
        flex-wrap: wrap !important;
        width: 100% !important;

        .form-row {
          display: flex;
          flex-direction: column;
          flex-basis: 100% !important;
          flex: 1;
          align-items: flex-start !important;

          .field-container {
            .name_field {
              width: 100% !important;

            }
          }

          .field-lbl {
            font-size: 0.813rem !important;
            line-height: 1rem !important;
          }

          .other-container {
            width: 100% !important;
            // display: flex;
            justify-content: space-between !important;
            // flex-direction: column;
            // margin: 1.5rem;

            .field-lbl-othr {
              font-size: 0.813rem !important;
              line-height: 1rem !important;
            }

            .mobile-wrapper {
              width: 100% !important;
              justify-content: space-between !important;

              .name_field-othr {
                box-sizing: border-box;
                width: 15rem !important;
                height: auto;
                margin-left: 0 !important;
                // border-bottom: 1px solid #ffffff;
              }
            }
          }
        }

        .form-row-last {
          margin: 0 2rem !important;
          justify-content: center !important;

          &.primary {
            font-family: "Noto Serif" !important;
            font-style: normal !important;
            font-weight: 600 !important;
            font-size: 1rem !important;
            line-height: 1.375rem !important;
          }
        }
      }
    }
  }
}
</style>
