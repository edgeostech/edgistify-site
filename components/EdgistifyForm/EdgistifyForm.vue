<template>
  <v-container fluid class="form-main pa-0">
    <form ref="inquiry" class="form_design" @submit.prevent="handleSubmit">
      <v-row no-gutters class="main-left">
        <h1>
          <!-- Get a Quote<br /> Now -->
          Get Started with <span style="color: #00a699">Edgistify</span>
        </h1>
        <p>
          Get a grip on your supply chain with a perfect blend of a consultative
          approach, operational excellence and technology. Talk to our Supply
          Chain Experts.
        </p>
      </v-row>
      <v-row no-gutters class="main-right">
        <v-col class="right-name">
          <v-col class="form-row px-0">
            <v-col class="field-container px-0 pl-md-10">
              <label class="field-lbl">Name *</label>
              <input
                type="text"
                id="name"
                name="name"
                v-model="name"
                class="name_field"
                required
              />
            </v-col>
            <v-col class="field-container px-0 pl-md-10">
              <label class="field-lbl">Company/Organization *</label>
              <input
                type="text"
                id="name"
                v-model="company"
                name="name"
                class="name_field"
                required
              />
            </v-col>
          </v-col>
          <v-col class="form-row px-0 email-box">
            <v-col class="field-container px-0 pl-md-10">
              <label class="field-lbl">Email *</label>
              <input
                type="text"
                id="name"
                name="name"
                v-model="email"
                class="name_field"
                required
              />
            </v-col>
            <v-col class="other-container px-0">
              <label class="field-lbl-othr">Phone number *</label>
              <v-col class="mobile-wrapper px-0">
                <!-- <select name="mobile" id="mobile" class="dropdown">
                  <option value="india">+91</option>
                </select> -->
                <v-select
                  :items="['+91']"
                  variant="underlined"
                  class="multi-select-white no-space"
                  style="width: 20%"
                ></v-select>
                <input
                  type="text"
                  id="name"
                  v-model="mobile"
                  name="name"
                  class="name_field-othr"
                  required
                />
              </v-col>
            </v-col>
          </v-col>
          <v-col
            class="form-row px-0 email-box"
            style="justify-content: flex-start"
          >
            <v-col class="field-container px-0 pl-md-10" md="6">
              <label class="field-lbl">Services Looking for*</label>

              <v-select
                v-model="favorites"
                :items="states"
                variant="underlined"
                class="multi-select-white no-space"
                multiple
                persistent-hint
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
            </v-col>
            <v-col class="form-row-last px-0">
              <v-col class="content-button">
                <v-btn
                  class="button bg-white"
                  data-aos="fade-up"
                  data-aos-once="true"
                  data-aos-easing="ease-in"
                  data-aos-duration="1000"
                  @click="handleSubmit"
                  >Submit</v-btn
                >
              </v-col>
            </v-col>
          </v-col>
        </v-col>
        <v-col md="12" sm="12" class="pl-md-10" v-if="showMsg">
          <p class="msg">Thank you! We'll be in touch shortly.</p>
        </v-col>
      </v-row>
    </form>

    <div>
      <NotifyModal v-show="showModal" @close-notify-modal="resetForm()" />
    </div>
  </v-container>
</template>

<script>
import NotifyModal from "../ModalForm/NotifyModal.vue";

export default {
  components: { NotifyModal },

  data() {
    return {
      name: "",
      email: "",
      mobile: "",
      company: "",
      showModal: false,
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
  methods: {
    async handleSubmit() {
      const data = {
        name: this.name,
        email: this.email,
        mobileNumber: `+91${this.mobile}`,
        organization: this.company,
        serviceRequested: this.favorites,
      };
      const res = await this.$axios.post("/inquiry", data);

      if (res.data.success) {
        this.showMsg = true;
      } else {
        this.showMsg = false;
      }
    },
    resetForm() {
      this.showModal = false;
      this.name = "";
      this.email = "";
      this.mobile = "";
      this.company = "";
      this.favorites = "";
    },
  },
};
</script>

<style scoped>
.theme--light.v-select .v-select__selections {
  color: white !important;
}
.multi-select .v-input__slot:before {
  border-color: white !important ;
}
.msg {
  font-family: "Noto Serif";
  font-style: normal;
  font-weight: 600;
  font-size: 42px;
  line-height: 50px;
  color: #313131;
  padding-bottom: 0 !important;
}

.multi-select-white.v-application .primary--text {
  color: #000000;
}

.v-application .primary--text {
  color: #000000 !important;
  caret-color: #000000 !important;
}
</style>

<style lang="scss" scoped>
@media (max-width: 850px) {
  .form_design {
    flex-wrap: wrap;
    margin-left: 0 !important;
    margin-right: 0 !important;
    padding-top: 12px !important;
  }
  .email-box {
    padding-top: 0;
    padding-bottom: 0;
    > .field-container {
      padding-top: 0 !important;
    }
  }
  .multi-select {
    padding-top: 0 !important;
  }
  .mobile-wrapper {
    .dropdown {
      width: 30% !important;
    }
  }

  .other-container {
    margin-left: 0 !important;
  }
  .form-main {
    display: flex !important;
    flex-direction: row !important;
    flex-wrap: wrap !important;
    width: 100% !important;
    height: auto !important;
    padding: 6% 6% !important;
  }

  .main-left {
    padding: 0 !important;

    width: 100% !important;
    height: auto !important;
  }

  .main-right {
    padding: 0 !important;
    .name_field-othr {
      height: 35px !important;
    }

    .mobile-wrapper {
      width: 100% !important;
      height: 64px;
      padding-top: 0;
      padding-bottom: 0;
    }
  }

  .right-name {
    display: flex !important;
    flex-direction: row !important;
    flex-wrap: wrap !important;
    width: 100% !important;

    .form-row {
      display: flex;
      flex-direction: column;
      flex-basis: 100% !important;
      align-items: flex-start !important;

      .field-container {
        .name_field {
          width: 100% !important;
        }
      }
    }

    .form-row-last {
      margin: 0 !important;
      height: auto !important;
    }
  }

  .content-button {
    padding: 2% 22% !important;
    justify-content: center !important;
  }
}

.form_design {
  display: flex;
  width: 100%;
  margin: 2% 6% 0 6%;
  border-top: 1px solid #8d8d8d;
}

.form-main {
  width: 100%;
  height: auto;
  display: flex;
  background: white;

  .main-left {
    width: 30%;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    height: auto;
    padding: 6% 0 6% 0;

    h1 {
      font-family: "Noto Serif";
      font-style: normal;
      font-weight: 600;
      font-size: 49.3107px;
      line-height: 55px;
      color: #313131;
    }

    p {
      font-family: "Outfit";
      font-style: normal;
      font-weight: 200;
      font-size: 16px;
      line-height: 20px;
      margin: 1rem 0 0 0;
      color: #313131;
    }
  }

  .main-right {
    width: 70%;
    height: auto;
    display: flex;
    padding: 6% 0 0 6%;

    .right-name {
      width: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;

      .form-row {
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;

        .field-container {
          display: flex;
          flex-direction: column;

          .name_field {
            box-sizing: border-box;
            height: auto;

            background: #fff;
            border-bottom: 1px solid #000;
          }

          .name_field:focus {
            outline: none;
            caret-color: #f3f5f3;
          }

          .name_field:hover {
            background: #ffffff;
          }

          .field-lbl {
            font-family: "Outfit";
            font-style: normal;
            font-weight: 400;
            font-size: 16px;
            line-height: 20px;
            color: #000;
          }

          .field-container {
            width: 156px;
            height: 44px;
            left: 1192px;
            top: 379px;
            background: #ffffff;
            border-radius: 44px;
          }
        }

        .other-container {
          display: flex;
          flex-direction: column;
          margin-left: 2.625rem;

          .field-lbl-othr {
            font-family: "Outfit";
            font-style: normal;
            font-weight: 400;
            font-size: 16px;
            line-height: 20px;
            color: #000;
          }

          .mobile-wrapper {
            display: flex;
            justify-content: space-between;

            .dropdown {
              outline: none;
              width: 20%;
              padding-left: 1.5rem;
              display: flex;
              color: #000;
              background-image: url("/Solutions/warehousing/down-arrow.png");
              background-position-y: center;
              background-position-x: 4rem;
              background-color: transparent;
              border-bottom: 1px solid #000;
            }

            .name_field-othr {
              box-sizing: border-box;
              width: 100%;
              height: 48px;
              background: white;
              margin-left: 20px;
              border-bottom: 1px solid #000;
            }

            .name_field-othr:focus {
              outline: none;
              caret-color: #f3f5f3;
            }
          }
        }
      }

      .form-row-last {
        display: flex;
        height: 100%;

        .content-button {
          display: flex;
          justify-content: flex-end;
          align-items: flex-end;
          padding: 0 0 5%;

          .button {
            display: flex;
            height: 40px;
            border-radius: 73px;
            font-family: "Noto Serif";
            text-transform: capitalize;
            font-style: normal;
            font-size: 14px;
            font-weight: 700;
            line-height: 25px;
            border: none;
            letter-spacing: 0px;
          }
        }
      }
    }
  }
}
</style>
