<template>
  <div class="modal-overlay">
    <!-- @click="$emit('close-modal')"  @click.stop -->
    <div class="modal">
      <div class="modal_left">
        <h1>
          Get started <br />
          with <span>Edgistify</span>
        </h1>
        <p>
          Tell us more about your logistics requirements so we can optimize your
          business and streamline operations for you. Get a grip on your supply
          chain with a perfect blend of technology and consultative approach.
          Talk to our supply chain experts.
        </p>
      </div>
      <div class="modal_right">
        <div class="modal_heading">
          <div class="modal_heading_title">
            <h1>Ready to Start a Hassle-free Fulfillment Journey?</h1>
          </div>
          <div class="close" @click="$emit('close-modal')">
            <v-img
              alt="close_icon"
              class="close_icon"
              src="/close_icon.png"
              contain
            />
          </div>
        </div>

        <div v-if="showMsg" class="msg-container pt-6">
          <p>
            Fill out the form and one of our sales representatives will be in
            touch with you shortly.
          </p>
          <h1 class="pt-3 pb-6">
            Thank you! <br />We'll be in <br />
            touch shortly.
          </h1>
          <a class="pt-3" href="#" @click="showMsg = false">Back to Form</a>
        </div>

        <!-- Web Layout -->
        <form
          class="form_design"
          @submit.prevent="handleSubmit"
          v-if="!showMsg && !isSmallDevice"
        >
          <div class="line_row">
            <div class="field_container">
              <label class="field_title">First Name *</label>
              <input
                v-model="fname"
                type="text"
                id="fname"
                class="name_field"
                required
              />
              <!-- <input type="text" id="fname" class="name_field" required> -->
            </div>
            <div class="field_container">
              <label class="field_title">Last Name</label>
              <input
                v-model="lname"
                type="text"
                id="lname"
                class="name_field"
              />
              <!-- id="lname" -->
            </div>
          </div>
          <div class="line_row">
            <div class="field_container">
              <label class="field_title">Email *</label>
              <input
                v-model="email"
                type="email"
                id="email"
                class="name_field"
                required
              />
              <!-- id="email" -->
            </div>
            <div class="field_container">
              <label class="field_title">Mobile Number *</label>
              <input
                v-model="mobile"
                type="text"
                id="mobile"
                class="name_field"
                required
              />
              <!-- id="mobile" -->
            </div>
          </div>
          <div class="line_row">
            <div class="field_container">
              <label class="field_title">Alternate Mobile</label>
              <input
                v-model="altmobile"
                type="text"
                id="altmobile"
                class="name_field"
              />
              <!-- id="altmobile" -->
            </div>
            <div class="field_container">
              <label class="field_title">Company/Organization *</label>
              <input
                v-model="company"
                type="text"
                id="company"
                class="name_field"
                required
              />
              <!-- id="company" -->
            </div>
          </div>
          <div class="line_row">
            <div class="field_container">
              <label class="field_title">Services Looking for*</label>
              <v-select
                v-model="favorites"
                :items="states"
                variant="underlined"
                color="#000"
                multiple
                style="height: 35px; padding-top: 0; margin-top: 0"
              >
                <template v-slot:selection="{ item, index }">
                  <v-chip v-if="index < 1">
                    <span>{{ item }}</span>
                  </v-chip>
                  <span
                    v-if="index === 1"
                    class="text-grey text-caption align-self-center"
                  >
                    (+{{ favorites.length - 1 }} others)
                  </span>
                </template>
              </v-select>
            </div>
            <div class="field_container">
              <label class="field_title">Extra Information</label>
              <input
                v-model="content"
                type="text"
                id="content"
                class="name_field"
                style="height: auto"
              />
              <!-- id="comment" -->
            </div>
          </div>
          <!-- <div class="line_row">
            <div class="field_container">
              <label class="field_title"><span>Schedule a Call with Our Experts or Call Now at +91-3334441111</span></label>
            </div>
          </div> -->

          <div class="line_row">
            <div class="field_container">
              <label class="field_title">Date</label>
              <input v-model="date" type="date" id="date" class="name_field" />
              <!-- id="Date" -->
            </div>
            <div class="field_container">
              <label class="field_title">Time</label>
              <input v-model="time" type="time" id="time" class="name_field" />
              <!-- id="time" -->
            </div>
          </div>
          <div class="form-btn">
            <div class="btn-container">
              <v-btn class="button primary" @click="handleSubmit">Submit</v-btn>
            </div>
          </div>
        </form>

        <!-- Mobile Layout -->
        <form
          class="form_design"
          @submit.prevent="handleSubmit"
          v-if="isSmallDevice && !showMsg"
        >
          <div class="line_row">
            <div class="field_container">
              <label class="field_title">First Name *</label>
              <input
                v-model="fname"
                type="text"
                id="fname"
                class="name_field"
                required
              />
            </div>
            <div class="field_container">
              <label class="field_title">Last Name</label>
              <input
                v-model="lname"
                type="text"
                id="lname"
                class="name_field"
              />
            </div>
            <div class="field_container">
              <label class="field_title">Email *</label>
              <input
                v-model="email"
                type="email"
                id="email"
                class="name_field"
                required
              />
            </div>
            <div class="field_container">
              <label class="field_title">Mobile Number *</label>
              <input
                v-model="mobile"
                type="text"
                id="mobile"
                class="name_field"
                required
              />
            </div>
            <div class="field_container">
              <label class="field_title">Alternate Mobile</label>
              <input
                v-model="altmobile"
                type="text"
                id="altmobile"
                class="name_field"
              />
            </div>
            <div class="field_container">
              <label class="field_title">Company/Organization *</label>
              <input
                v-model="company"
                type="text"
                id="company"
                class="name_field"
                required
              />
            </div>
            <div class="field_container">
              <label class="field_title">Services Looking for*</label>

              <v-select
                v-model="favorites"
                :items="states"
                class="no-space"
                variant="underlined"
                multiple
              >
                <template v-slot:selection="{ item, index }">
                  <v-chip v-if="index < 1">
                    <span>{{ item }}</span>
                  </v-chip>
                  <span
                    v-if="index === 1"
                    class="text-grey text-caption align-self-center"
                  >
                    (+{{ favorites.length - 1 }} others)
                  </span>
                </template>
              </v-select>
            </div>
            <div class="field_container extra">
              <label class="field_title">Extra Information</label>
              <input
                v-model="content"
                type="text"
                id="content"
                class="name_field"
                style="height: auto"
              />
            </div>
            <!-- <div class="field_container">
              <label class="field_title"><span>Schedule a Call with Our Experts or Call Now at +91-3334441111</span></label>
            </div> -->
            <div class="field_container">
              <label class="field_title">Date</label>
              <input v-model="date" type="date" id="date" class="name_field" />
            </div>
            <div class="field_container">
              <label class="field_title">Time</label>
              <input v-model="time" type="time" id="time" class="name_field" />
            </div>
            <div class="form-btn">
              <div class="btn-container">
                <button
                  @click="$emit('close-modal')"
                  type="submit"
                  class="button btn-white"
                >
                  Submit
                </button>
              </div>
            </div>
          </div>
        </form>
        <div>
          <NotifyModal v-show="showModal" @close-notify-modal="resetForm()" />
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.msg-container {
  padding-left: 3%;
  p {
    font-family: "Outfit";
    font-style: normal;
    font-weight: 400;
    font-size: 24px;
    line-height: 30px;

    color: #313131;
  }
  h1 {
    font-family: "Noto Serif";
    font-style: normal;
    font-weight: 600;
    font-size: 54.8709px;
    line-height: 75px;

    color: #0c0c0c;
  }
  a {
    font-family: "Outfit";
    font-style: normal;
    font-weight: 400;
    font-size: 24px;
    line-height: 30px;
    text-decoration-line: underline;

    color: #00a699;
  }
}
.multi-select > .v-input__control > .v-input__slot:before {
  border-color: white !important;
}
.modal-overlay {
  display: flex;
  position: fixed;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  z-index: 4;
  height: 100vh;
  width: 100%;
  transition: all 0.5s ease-in-out;

  .modal {
    display: flex;
    width: 100%;
    height: 100%;
    z-index: 1;
    vertical-align: initial;

    .modal_left {
      display: flex;
      flex-direction: column;
      background-color: #000000;
      height: 100%;
      width: 34%;
      position: relative;
      padding: 2.8% 3.75% 0 3.75%;

      h1 {
        position: relative;
        font-family: "Noto Serif";
        font-style: normal;
        font-weight: 600;
        font-size: 54.8709px;
        line-height: 75px;
        color: white !important;

        span {
          color: #00a699;
        }
      }

      p {
        position: relative;
        // width: 378px;
        // height: 100px;
        // left: 54px;
        padding-top: 5%;
        font-family: "Outfit";
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        line-height: 20px;
        color: #ffffff;
      }
    }

    .modal_right {
      display: flex;
      flex-direction: column;
      background-color: #ffffff;
      height: 100%;
      width: 66%;
      padding: 3% 2% 1% 2%;

      .modal_heading {
        display: flex;
        flex-direction: row;
        gap: 18%;
        padding-left: 3%;

        .modal_heading_title {
          position: relative;

          h1 {
            // position: absolute;
            // width: 831px;
            // height: 49px;
            // left: 539px;
            // top: 57px;
            font-family: "Noto Serif";
            font-style: normal;
            font-weight: 500;
            font-size: 36px;
            line-height: 49px;
            color: #0c0c0c;
          }
        }

        .close {
          align-items: center;
          cursor: pointer;

          .close_icon {
            display: flex;
            position: relative;
            // align-items: center;
            // justify-content: right;
            // top: 45px;
            // left: 950px;
          }
        }
      }

      .form_design {
        display: flex;
        flex-direction: column;
        justify-content: center;
        // width: 100%;
        // justify-content: center;
        align-items: center;
        padding: 3% 3% 3% 3%;

        .line_row {
          width: 100%;
          display: flex;
          flex-direction: row;
          // align-items: center;
          position: relative;
          gap: 20%;

          // justify-content: center;
          .field_container {
            position: relative;
            width: 80%;
            display: flex;
            flex-direction: column;
            margin: 3% 0 0 0;
            gap: 20%;

            .field_title {
              // width: 100%;
              position: relative;
              height: 30px;
              font-family: "Outfit";
              font-style: normal;
              font-weight: 400;
              font-size: 16px;
              // line-height: 20px;
              color: #0c0c0c;

              span {
                // width: 200px;
                // height: 20px;
                font-family: "Outfit";
                position: relative;
                font-style: normal;
                font-weight: 600;
                font-size: 1rem;
                // line-height: 25px;
                color: #00a699;
                // margin-top: 20%;
              }

              select {
                width: 100%;
                appearance: none;
                background-image: url("/dropdown-arrow.png");
                background-repeat: no-repeat;
                background-position: right center;
                // padding-right: 20px;
              }
            }

            .name_field {
              box-sizing: border-box;
              width: 100%;
              height: 120%;
              border-bottom: 1px solid #000000;
            }
          }
        }

        .form-btn {
          width: 100%;
          display: flex;
          margin: 6% 0 0 0;
          justify-content: flex-end;

          .btn-container {
            display: flex;
            width: 156px;
            height: 44px;

            .button {
              width: 100%;
              font-style: normal;
              font-weight: 600;
              line-height: 20px;
              color: #ffffff;
              background: #00a699 !important;
              border-radius: 44px;
              font-family: "Noto Serif";
              font-size: 16px;
              text-transform: unset !important;
            }
          }
        }
      }
    }
  }
}

body.modal-overlay -open {
  overflow: show;
}

@media screen and (max-width: 850px) {
  .modal-overlay {
    display: flex;
    position: fixed;
    z-index: 4;
    height: auto !important;
    width: 100%;

    .modal {
      display: flex;
      width: 100%;
      flex-direction: column !important;
      height: auto !important;
      z-index: 1;
      vertical-align: initial;
      overflow-y: auto !important;

      .modal_left {
        display: flex;
        flex-direction: column;
        background-color: #000000;
        height: 100%;
        width: 100% !important;
        position: relative;
        padding: 18% 3.75% 0 3.75% !important;

        h1 {
          position: relative;
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 600;
          font-size: 2.25rem !important;
          line-height: 3.063rem !important;

          span {
            color: #00a699;
          }
        }

        p {
          position: relative;
          padding-top: 5%;
          padding-bottom: 5% !important;
          font-family: "Outfit";
          font-style: normal;
          font-weight: 400;
          font-size: 0.75rem !important;
          line-height: 0.938rem !important;
          color: #ffffff;
        }
      }

      .modal_right {
        display: flex;
        flex-direction: column;
        background-color: #ffffff;
        height: auto !important;
        width: 100% !important;
        padding: 3% 2% 1% 2%;

        .modal_heading {
          display: flex;
          flex-direction: row;
          gap: 10%;
          width: 100% !important;

          .modal_heading_title {
            position: relative;
            padding-left: 4% !important;
            width: 100% !important;
            padding-left: 0 !important;

            h1 {
              font-family: "Noto Serif";
              font-style: normal;
              font-weight: 500;
              font-size: 1.5rem !important;
              line-height: 2.063rem !important;
              color: #0c0c0c;
            }
          }

          .close {
            align-items: center;
            cursor: pointer;

            .close_icon {
              display: flex;
              position: relative;
            }
          }
        }

        .form_design {
          display: flex;
          flex-direction: column;
          justify-content: center;
          align-items: center;
          padding: 3% 3% 3% 3%;
          height: auto !important;

          .line_row {
            width: 100%;
            display: flex;
            height: fit-content !important;
            flex-direction: column !important;
            position: relative;
            gap: 0% !important;

            .field_container.extra {
              margin-top: 0 !important;
            }
            .field_container {
              position: relative;
              width: 90% !important;
              display: flex;
              flex-direction: column;
              margin: 5% 0 0 0 !important;
              gap: 10% !important;

              .field_title {
                position: relative;
                height: 30px;
                font-family: "Outfit";
                font-style: normal;
                font-weight: 400;
                font-size: 0.813rem !important;
                color: #0c0c0c;
                margin: 8px 0;

                span {
                  font-family: "Outfit";
                  position: relative;
                  font-style: normal;
                  font-weight: 600;
                  font-size: 1rem;
                  color: #00a699;
                }

                select {
                  width: 100%;
                  appearance: none;
                  background-image: url("/dropdown-arrow.png");
                  background-repeat: no-repeat;
                  background-position: right center;
                }
              }

              .name_field {
                box-sizing: border-box;
                width: 100%;
                height: 120%;
                border-bottom: 1px solid #000000;
              }
            }
          }

          .form-btn {
            width: 100%;
            display: flex;
            margin: 6% 0 0 0;

            justify-content: center;

            .btn-container {
              display: flex;
              width: 156px;
              height: 44px;

              .button {
                width: 100%;
                font-style: normal;
                color: #ffffff;
                background: #00a699 !important;
                border-radius: 44px;
                font-family: "Noto Serif";
                font-size: 14px !important;
                line-height: 20px !important;
                font-weight: 300 !important;
                text-transform: unset !important;
              }
            }
          }
        }
      }
    }
  }
}
</style>

<script>
import NotifyModal from "./NotifyModal.vue";

export default {
  components: { NotifyModal },

  data() {
    return {
      fname: "",
      lname: "",
      email: "",
      mobile: "",
      altmobile: "",
      company: "",
      services: "",
      content: "",
      date: "",
      time: "",
      showModal: false,
      isSmallDevice: false,
      showMsg: false,
      favorites: [],
      states: [
        "Supply Chain Consulting",
        "E-commerce Fulfillment",
        "Warehouse Operations",
        "Hyperlocal & Same Day Delivery",
        "Supply Chain Technology (WMS/OMS)",
        "Logistics & Transportation",
      ],
    };
  },
  mounted() {
    if (window.innerWidth <= 850) {
      this.isSmallDevice = true;
    } else {
      this.isSmallDevice = false;
    }
  },
  methods: {
    async handleSubmit() {
      console.log(this.favorites);
      const date = this.date.split("-");
      const time = this.time.split(":");
      const appointment = new Date(
        date[0],
        date[1],
        date[2],
        time[0],
        time[1],
        0
      );

      const data = {
        name: `${this.fname} ${this.lname}`,
        email: this.email,
        mobileNumber: this.mobile,
        alternateMobileNumber: this.altmobile,
        organization: this.company,
        serviceRequested: this.favorites,
        comment: this.content,
        appointment,
      };
      const res = await this.$axios.post("/inquiry", data);
      if (res.data.success) {
        this.showMsg = true;
      } else {
        this.showMsg = false;
      }
    },
    resetForm: function () {
      this.showModal = false;
      this.fname = "";
      this.lname = "";
      this.email = "";
      this.mobile = "";
      this.altmobile = "";
      this.company = "";
      this.favorites = "";
      this.content = "";
      this.date = "";
      this.time = "";
    },
  },
};
</script>
