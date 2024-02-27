<template>
  <v-container fluid class="careers pa-0">
    <v-row
      class="mb-6 careers-wrapper"
      style="background: white"
      justify="center"
      no-gutters
      id="careers-joinus"
    >
      <v-col sm="12" md="12" lg="12">
        <p class="text">
          At Edgistify, we love solving complex supply chain challenges that
          have a real impact on businesses and their customers. If you possess a
          mindset<br />
          focused on delivering results and a passion for bringing innovative
          concepts to life, then Edgistify is the ideal place to build your
          career.<br />
        </p>

        <h3>Be Part of a Passionate, Energetic and Synergetic Team</h3>
      </v-col>
      <v-col lg="12" sm="12" md="12">
        <div class="blank-div">
          <v-img src="/Company/edgistify-team.jpg.jpg" alt="Edgistify team of supply chain specialists working together to provide innovative solutions for businesses" class="img"></v-img>
        </div>
      </v-col>
      <v-col lg="12" sm="12" md="12">
        <div class="section-perks" v-if="!isSmallDevice">
          <h1 class="page-title">Perks</h1>
          <v-row
            no-gutters
            class="careers-wrapper-row1"
            justify="space-between"
          >
            <v-col cols="6" lg="2" sm="6">
              <div class="specialists-details">
                <v-img src="/career/Group.png" class="img"></v-img>
                <div class="info-text">
                  <p>
                    Competitive<br />
                    Salaries
                  </p>
                </div>
              </div>
            </v-col>
            <v-col cols="6" lg="2" sm="6">
              <div class="specialists-details">
                <v-img src="/career/Group (22).png" class="img"></v-img>
                <div class="info-text">
                  <p>
                    Half Yearly <br />
                    Off-sites
                  </p>
                </div>
              </div>
            </v-col>
            <v-col cols="6" lg="2" sm="6">
              <div class="specialists-details">
                <v-img src="/career/Group (2).png" class="img"></v-img>
                <div class="info-text">
                  <p>
                    Medical<br />
                    Insurance
                  </p>
                </div>
              </div>
            </v-col>
            <v-col cols="6" lg="2" sm="6">
              <div class="specialists-details">
                <v-img src="/career/Group (3).png" class="img"></v-img>
                <div class="info-text">
                  <p>
                    Learning budget for<br />
                    personal development
                  </p>
                </div>
              </div>
            </v-col>
            <v-col cols="6" lg="2" sm="6">
              <div class="specialists-details">
                <v-img src="/career/Group (4).png" class="img"></v-img>
                <div class="info-text">
                  <p>
                    Quarterly Evaluation<br />
                    for Growth
                  </p>
                </div>
              </div>
            </v-col>
          </v-row>
          <v-row
            no-gutters
            class="careers-wrapper-row1 margin-top"
            justify="space-between"
          >
            <v-col cols="6" lg="2" sm="6">
              <div class="specialists-details">
                <v-img src="/career/Group (5).png" class="img"></v-img>
                <div class="info-text">
                  <p>
                    Annual<br />
                    Appraisals
                  </p>
                </div>
              </div>
            </v-col>
            <v-col cols="6" lg="2" sm="6">
              <div class="specialists-details">
                <v-img src="/career/Group (6).png" class="img"></v-img>
                <div class="info-text">
                  <p>
                    Recreational<br />
                    Area
                  </p>
                </div>
              </div>
            </v-col>
            <v-col cols="6" lg="2" sm="6">
              <div class="specialists-details">
                <v-img src="/career/Group (7).png" class="img"></v-img>
                <div class="info-text">
                  <p>
                    Annual<br />
                    Celebrations
                  </p>
                </div>
              </div>
            </v-col>
            <v-col cols="6" lg="2" sm="6">
              <div class="specialists-details">
                <v-img src="/career/Group (8).png" class="img"></v-img>
                <div class="info-text">
                  <p>
                    Well-Planned<br />
                    Leave Policy
                  </p>
                </div>
              </div>
            </v-col>
            <v-col cols="6" lg="2" sm="6">
              <div class="specialists-details">
                <v-img src="/career/Group (23).png" class="img"></v-img>
                <div class="info-text">
                  <p>
                    Loaded<br />
                    Pantry
                  </p>
                </div>
              </div>
            </v-col>
          </v-row>
        </div>
        <!-- Mobile Layout -->
        <div class="section-perks" v-if="isSmallDevice">
          <h1 class="page-title">Perks</h1>
          <div class="container">
            <v-row
              class="careers-wrapper-row1"
              no-gutters
              justify="space-between"
            >
              <v-col cols="6" lg="2" sm="2">
                <div class="specialists-details">
                  <v-img src="/career/Group.png" class="img"></v-img>
                  <div class="info-text">
                    <p>
                      Competitive<br />
                      Salaries
                    </p>
                  </div>
                </div>
              </v-col>

              <v-col cols="6" lg="2" sm="2">
                <div class="specialists-details">
                  <v-img src="/career/Group (22).png" class="img"></v-img>
                  <div class="info-text">
                    <p>
                      Half Yearly <br />
                      Off-sites
                    </p>
                  </div>
                </div>
              </v-col>
              <v-col cols="6" lg="2" sm="2">
                <div class="specialists-details">
                  <v-img src="/career/Group (2).png" class="img"></v-img>
                  <div class="info-text">
                    <p>
                      Medical<br />
                      Insurance
                    </p>
                  </div>
                </div>
              </v-col>
              <v-col cols="6" lg="2" sm="2">
                <div class="specialists-details">
                  <v-img src="/career/Group (3).png" class="img"></v-img>
                  <div class="info-text">
                    <p>
                      Learning budget for<br />
                      personal development
                    </p>
                  </div>
                </div>
              </v-col>
              <v-col cols="6" lg="2" sm="2">
                <div class="specialists-details">
                  <v-img src="/career/Group (4).png" class="img"></v-img>
                  <div class="info-text">
                    <p>
                      Quarterly Evaluation<br />
                      for Growth
                    </p>
                  </div>
                </div>
              </v-col>
              <v-col cols="6" lg="2" sm="2">
                <div class="specialists-details">
                  <v-img src="/career/Group (5).png" class="img"></v-img>
                  <div class="info-text">
                    <p>
                      Annual<br />
                      Appraisals
                    </p>
                  </div>
                </div>
              </v-col>
              <v-col cols="6" lg="2" sm="2">
                <div class="specialists-details">
                  <v-img src="/career/Group (6).png" class="img"></v-img>
                  <div class="info-text">
                    <p>
                      Recreational<br />
                      Area
                    </p>
                  </div>
                </div>
              </v-col>
              <v-col cols="6" lg="2" sm="2">
                <div class="specialists-details">
                  <v-img src="/career/Group (7).png" class="img"></v-img>
                  <div class="info-text">
                    <p>
                      Annual<br />
                      Celebrations
                    </p>
                  </div>
                </div>
              </v-col>
              <v-col cols="6" lg="2" sm="2">
                <div class="specialists-details">
                  <v-img src="/career/Group (8).png" class="img"></v-img>
                  <div class="info-text">
                    <p>
                      Well-Planned<br />
                      Leave Policy
                    </p>
                  </div>
                </div>
              </v-col>

              <v-col cols="6" lg="2" sm="2">
                <div class="specialists-details">
                  <v-img src="/career/Group (23).png" class="img"></v-img>
                  <div class="info-text">
                    <p>
                      Loaded<br />
                      Pantry
                    </p>
                  </div>
                </div>
              </v-col>
            </v-row>
          
          </div>
        </div>
        <!-- Mobile End -->
      </v-col>
    </v-row>
  </v-container>
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
  .page-title {
    font-size: 30px !important;
  }
  .careers {
    width: 100% !important;
    height: auto !important;

    .careers-wrapper {
      p {
        font-family: "Outfit" !important;
        font-size: 16px !important;
        line-height: 20px !important;
        text-align: center !important;
        color: #313131 !important;
        padding: 0 30px;
      }

      h3 {
        font-family: "Noto Serif" !important;
        font-style: normal !important;
        font-weight: 400 !important;
        font-size: 24px !important;
        line-height: 33px !important;
        text-align: center !important;
        color: #161616 !important;
        padding: 0 30px;
      }

      .blank-div {
        height: 134px !important;
        padding: 0 30px !important;
      }
    }

    .section-perks {
      h1 {
        font-family: "Noto Serif" !important;
        font-style: normal !important;
        font-weight: 400 !important;
        font-size: 2rem !important;
        line-height: 33px !important;
        text-align: left !important;
        color: #161616 !important;
        padding-left: 0rem !important;
        margin: 30px !important;
      }

      .container {
        padding: 0;

        .col-6 {
          padding-right: 8px;
          padding-bottom: 8px;
        }

        .margin-top {
          margin-top: 0 !important;
        }

        .careers-wrapper-row1 {
          .specialists-details {
            background: #f3f3f5;

            .img {
              width: 45.77px !important;
              margin-bottom: 0.5rem;
            }

            .info-text {
              width: 100%;
              margin: 1.5rem 0 0 0;

              p {
                font-family: "Outfit" !important;
                font-style: normal !important;
                font-weight: 400 !important;
                font-size: 10.0205px !important;
                line-height: 13px !important;
                text-align: center !important;
                color: #313131 !important;
                padding: 0 !important;
              }
            }
          }
        }
      }
    }
  }
}

.careers {
  .page-title {
    font-size: 42px !important;
  }
  width: 100%;
  height: auto;
  padding: 0;

  .careers-wrapper {
    background: white;
    padding: 50px 0;

    h3 {
      font-family: "Noto Serif";
      font-style: normal;
      font-weight: 400;
      font-size: 35.4224px;
      line-height: 48px;
      color: #161616;
      margin-top: 1rem;
      text-align: center;
      margin-bottom: 50px;
    }

    p {
      font-family: "Outfit";
      font-style: normal;
      font-weight: 300;
      font-size: 18px;
      line-height: 23px;
      text-align: center;

      color: #313131;
    }

    .blank-div {
      padding: 0 6%;
      background: white;
      width: auto;
    }
  }

  .section-perks {
    display: flex;
    flex-direction: column;

    h1 {
      font-family: "Noto Serif";
      font-style: normal;
      font-weight: 400;
      font-size: 42.13px;
      line-height: 57px;
      margin: 3% 6%;
      text-align: left;
      color: #161616;
    }

    .margin-top {
      margin-top: 3em !important;
    }

    .careers-wrapper-row1 {
      margin: 0 6%;

      .specialists-details {
        height: 225px;
        background: #f3f3f5;
        padding: 36px;

        .img {
          width: 65.83px;
          margin-bottom: 0.5rem;
          margin: auto;
        }

        .info-text {
          width: 100%;
          margin: 1.5rem 0 0 0;

          p {
            font-family: "Outfit";
            font-style: normal;
            font-weight: 400;
            font-size: 16px;
            line-height: 20px;
            text-align: center;
            color: #313131;
          }
        }
      }
    }
  }
}
</style>
