<template>
  <v-container fluid class="warehouse-space-main">
    <v-row no-gutters class="main_title" id="warehouse-space">
      <h1>Talk to Our Supply Chain Experts!</h1>
    </v-row>
    <form
      ref="inquiry"
      class="form_design"
      @submit.prevent="handleSubmit"
      v-if="!isSmallDevice"
    >
      <v-row no-gutters class="form-container">
        <v-row no-gutters class="form-row">
          <v-col cols="12" md="5" sm="12" class="field-container py-6">
            <label class="field-lbl">Name *</label>
            <input
              v-model="name"
              type="text"
              id="name"
              name="name"
              class="name_field"
              required
            />
          </v-col>
          <v-col cols="12" md="5" sm="12" class="field-container py-6">
            <label class="field-lbl">Designation *</label>
            <input
              v-model="designation"
              type="text"
              id="name"
              name="name"
              class="name_field"
              required
            />
          </v-col>
          <!-- </v-col> -->
          <!-- <v-col class="form-row"> -->
          <v-col cols="12" md="5" sm="12" class="field-container py-6">
            <label class="field-lbl">Official e-mail *</label>
            <input
              v-model="email"
              type="email"
              id="name"
              name="name"
              class="name_field"
              required
            />
          </v-col>
          <v-col cols="12" md="5" sm="12" class="field-container py-6">
            <label class="field-lbl">Phone number *</label>
            <v-col class="mobile-wrapper pa-0">
              <!-- <select name="mobile" id="mobile" class="dropdown">
                <option value="india">+91</option>
              </select> -->
              <v-select
                :items="['+91']"
                variant="underlined"
                class="multi-select"
                color="white"
                style="margin-top: -10px; width: 20%; padding-right: 40px"
              ></v-select>
              <input
                v-model="mobile"
                type="text"
                id="name"
                name="name"
                class="name_mob_field"
                required
              />
            </v-col>
          </v-col>
          <!-- </v-col> -->
          <!-- <v-col class="form-row"> -->
          <v-col cols="12" md="5" sm="12" class="field-container py-6">
            <label class="field-lbl">Company/Organization *</label>
            <input
              v-model="company"
              type="text"
              id="name"
              name="name"
              class="name_field"
              required
            />
          </v-col>
          <v-col cols="12" md="5" sm="12" class="field-container py-6">
            <label class="field-lbl">Services Looking for*</label>
            <v-select
              v-model="favorites"
              :items="states"
              variant="underlined"
              class="multi-select"
              multiple
              base-color="white"
              color="white"
              style="margin-top: -10px"
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
              </template></v-select
            >
          </v-col>
          <!-- </v-col> -->
          <!-- <v-col class="form-row"> -->
          <v-col cols="12" md="5" sm="12" class="field-container py-6">
            <label class="field-lbl">Industry *</label>
            <input
              v-model="industry"
              type="text"
              id="name"
              name="name"
              class="name_field"
              required
            />
          </v-col>
          <v-col cols="12" md="5" sm="12" class="field-container py-6">
            <label class="field-lbl">Extra information </label>
            <input
              v-model="extraInformation"
              type="text"
              id="name"
              name="name"
              class="name_field"
              required
            />
          </v-col>
          <!-- </v-col> -->
          <!-- <v-col class="form-row-last"> -->
          <v-col cols="12" md="5" sm="12" class="btn-container">
            <v-btn
              class="contact-us button bg-black"
              data-aos-once="true"
              data-aos-easing="ease-in"
              data-aos-duration="1000"
              @click="this.handleSubmit"
            >
              Submit
            </v-btn>
          </v-col>
          <v-col sm="12" ms="12" class="msg pt-6" v-if="showMsg">
            <p>Thank you! We'll be in touch shortly.</p>
            <span
              >One of our sales representatives will be in touch with you
              shortly.</span
            >
          </v-col>
        </v-row>
      </v-row>
    </form>
    <div>
      <NotifyModal v-show="showModal" @close-notify-modal="resetForm()" />
    </div>
  </v-container>
</template>

<script>
import NotifyModal from "../../ModalForm/NotifyModal.vue";

export default {
  components: { NotifyModal },

  data() {
    return {
      name: "",
      designation: "",
      email: "",
      mobile: "",
      company: "",
      intresetedIn: "",
      industry: "",
      extraInformation: "",
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
        mobileNumber: this.mobile,
        designation: this.designation,
        organization: this.company,
        serviceRequested: this.favorites,
        industry: this.industry,
        comment: this.extraInformation,
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
      this.name = "";
      this.email = "";
      this.mobile = "";
      this.designation = "";
      this.company = "";
      this.favorites = "";
      this.industry = "";
      this.extraInformation = "";
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
</style>

<style lang="scss" scoped>
input {
  color: #ffffff;
}

.multi-select.v-application .primary--text {
  color: #ffffff;
  caret-color: #ffffff !important;
}

@media (max-width: 850px) {
  .warehouse-space-main {
    .main_title {
      padding: 2% 6% !important;

      h1 {
        font-family: "Noto Serif" !important;
        font-style: normal !important;
        font-weight: 400 !important;
        font-size: 30px !important;
        line-height: 33px !important;
        color: #ffffff !important;
      }
    }

    .form-container {
      .mobile-wrapper {
        justify-content: space-between !important;

        .dropdown {
          width: 7rem !important;
        }

        .name_mob_field {
          width: 60% !important;
        }
      }
    }
  }
}

.msg {
  display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  p {
    font-family: "Noto Serif";
    font-style: normal;
    font-weight: 500;
    font-size: 36px;
    line-height: 49px;
    color: #ffffff;
    margin-bottom: 0;
  }
  span {
    font-family: "Outfit";
    font-style: normal;
    font-weight: 400;
    font-size: 24px;
    line-height: 30px;
    color: #8d8d8d;
  }
}
.warehouse-space-main {
  height: auto;
  background: black;

  .main_title {
    padding: 2% 10%;
    display: flex;
    justify-content: center;
    h1 {
      font-family: "Noto Serif";
      font-style: normal;
      font-weight: 400;
      font-size: 42px;
      line-height: 57px;
      color: #ffffff;
    }
  }

  .form-container {
    height: auto;
    padding: 4% 6%;

    input,
    select,
    textarea {
      color: #ffffff;
    }

    .form-row {
      display: flex;
      align-items: flex-start;
      justify-content: center;
      gap: 3%;

      .field-container {
        display: flex;
        flex-direction: column;
        font-size: 28.5px;

        .field-lbl {
          font-family: "outfit";
          font-style: normal;
          font-weight: 400;
          font-size: 16px;
          line-height: 20px;
          color: white;
        }

        .mobile-wrapper {
          font-size: 17px;
          display: flex;

          .dropdown {
            width: 7rem;
            outline: none;
            text-align: center;
            display: flex;
            color: #ffffff;
            background-image: url("/Solutions/warehousing/down-arrow.png");
            background-position-y: center;
            background-position-x: 90px;
            background-color: transparent;
            border-bottom: 1px solid #ffffff;
            margin-right: 1rem;
          }

          .name_mob_field {
            width: 90%;
            display: block;
            border-bottom: 1px solid #ffffff;
            height: 2.188rem;

            &:focus-visible {
              border: none;
              border-bottom: 1px solid #ffffff;
              outline: 0;
            }
          }
        }
      }

      input {
        display: block;
        border-bottom: 1px solid #ffffff;
        height: 2.188rem;

        &:focus-visible {
          border: none;
          border-bottom: 1px solid #ffffff;
          outline: 0;
        }
      }
    }

    .btn-container {
      display: flex;
      justify-content: center;
      align-items: flex-start;
      padding-top: 6% !important;

      .contact-us {
        background: #00a699;
        border-radius: 44px;
        height: 44px;
        width: 156px;
        letter-spacing: 0px;
        text-transform: capitalize;
        color: #ffffff;
      }
    }
  }
}
</style>
