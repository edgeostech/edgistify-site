<template>
  <v-container fluid class="footer-container pa-0">
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row no-gutters class="footer-content">
      <v-col class="logo-container">
        <h1><span>Edg</span>e Log<span>isti</span>cs Simpli<span>fy</span>.</h1>
      </v-col>
      <v-col class="content-container" v-if="!isDevice">
        <v-col class="links-container">
          <v-col class="page-link-container">
            <ul>
              <li>
                <div class="list-container">
                  <nuxt-link :to="{ path: '/' }" style="text-decoration: none; color: inherit">
                    <p>Home</p>
                  </nuxt-link>
                </div>
              </li>
              <li>
                <div class="list-container">
                  <nuxt-link :to="{ path: '/company/the-leader-in-supply-chain-management-edgistify', hash: '#our-advisors' }"
                    style="text-decoration: none; color: inherit">
                    <p>Mentors</p>
                  </nuxt-link>
                </div>
              </li>
              <li>
                <div class="list-container">
                  <nuxt-link :to="{ path: '/company/the-leader-in-supply-chain-management-edgistify', hash: '#our-team' }" style="text-decoration: none; color: inherit">
                    <p>Team</p>
                  </nuxt-link>
                </div>
              </li>
              <li>
                <div class="list-container">
                  <nuxt-link :to="{ path: '/careers/exciting-opportunities-join-the-team-edgistify', hash: '#careers-container' }"
                    style="text-decoration: none; color: inherit">
                    <p>Careers</p>
                  </nuxt-link>
                </div>
              </li>
              <li>
                <div class="list-container" @click="showModal = true">
                  <p>Contact Us</p>
                </div>
              </li>
            </ul>
          </v-col>
          <v-col class="refrence-link-container">
            <ul>
              <li>
                <div class="list-container">
                  <nuxt-link :to="{ path: '/resources/access-the-tools-you-need-to-learn-resources-edgistify' }" style="text-decoration: none; color: inherit">
                    <p>Newsroom</p>
                  </nuxt-link>
                </div>
              </li>
              <li>
                <div class="list-container">
                  <nuxt-link :to="{ path: '/resources/access-the-tools-you-need-to-learn-resources-edgistify', hash: '#resource-media' }"
                    style="text-decoration: none; color: inherit">
                    <p>Awards</p>
                  </nuxt-link>
                </div>
              </li>

              <li>
                <div class="list-container">
                  <nuxt-link :to="{ path: '/resources/access-the-tools-you-need-to-learn-resources-edgistify', hash: '#resource-media' }"
                    style="text-decoration: none; color: inherit">
                    <p>Media and Mentions</p>
                  </nuxt-link>
                </div>
              </li>
            </ul>
          </v-col>
          <v-col class="social-media-link-container">
            <ul>
              <li>Follow Us</li>
              <li>
                <a href="https://in.linkedin.com/company/edgistify" target="_blank"><font-awesome-icon
                    :icon="['fab', 'linkedin']" class="icon" /></a>
                <a href="https://www.instagram.com/edgistify/?hl=en" target="_blank"><font-awesome-icon
                    :icon="['fab', 'square-instagram']" class="icon" /></a>
                <a href="https://www.facebook.com/edgistify/" target="_blank"><font-awesome-icon
                    :icon="['fab', 'square-facebook']" class="icon" /></a>
              </li>
              <li>
                <a href="https://twitter.com/edgistify?lang=en" target="_blank"><font-awesome-icon
                    :icon="['fab', 'twitter']" class="icon" /></a>
                <a href="https://www.youtube.com/c/Edgistify" target="_blank"><font-awesome-icon
                    :icon="['fab', 'youtube']" class="icon" /></a>
              </li>
            </ul>
          </v-col>
        </v-col>
        <v-col class="news-letter-signup-container">
          <div>
            <span> Sign up to our newsletter and stay updated.</span>
          </div>
          <div class="input-container">
            <v-text-field solo flat dense placeholder="Enter Your e-mail" style="
                height: 2.5rem;
                border-radius: 21px 0 0 21px;
                font-size: 13px;
              " hide-spin-buttons />
            <v-btn class="bg-black" dark width="80px" height="38px" depressed color="#00A699" style="
                border-radius: 0 21px 21px 0;
                margin-left: 1px;
                font-size: 13px;
                text-transform: capitalize;
              ">Sign Up</v-btn>
          </div>
        </v-col>
        <v-col class="help-container pa-0">
          <nuxt-link
                :to="{
                  path: '/Privacy',
                }"
                @click.native="scrollToLocation"
                style="text-decoration: none; color: inherit"
              >
              <span>Privacy Policy</span>

              </nuxt-link>          
              <nuxt-link
                :to="{
                  path: '/Terms',
                }"
                @click.native="scrollToLocation"
                style="text-decoration: none; color: inherit"
              >
              <span>Terms and Conditions</span>

              </nuxt-link>
              <nuxt-link
                :to="{
                  path: '/Sitemap',
                }"
                @click.native="scrollToLocation"
                style="text-decoration: none; color: inherit"
              >
              <span>Sitemap</span>

              </nuxt-link>
              
        </v-col>
      </v-col>
      <!-- Mobile Layout -->
      <v-col class="content-container" v-if="isDevice">
        <v-col class="news-letter-signup-container px-0">
          <v-col class="px-0">
            <span> Sign up to our newsletter to stay updated about us.</span>
          </v-col>
          <v-col class="input-container px-0">
            <v-text-field solo flat dense placeholder="Enter Your e-mail" style="
                max-width: 300px;
                height: 40px;
                border-radius: 21px 0 0 21px;
                font-size: 13px;
              " hide-spin-buttons />
            <v-btn dark width="80px" height="38px" depressed color="#00A699" style="
                border-radius: 0 21px 21px 0;
                margin-left: 1px;
                font-size: 13px;
                text-transform: capitalize;
              ">Sign Up</v-btn>
          </v-col>
        </v-col>
        <v-col class="links-container px-0">
          <v-col class="page-link-container px-0">
            <ul>
              <li>
                <div class="list-container">
                  <nuxt-link :to="{ path: '/' }" style="text-decoration: none; color: inherit">
                    Home
                  </nuxt-link>
                </div>
              </li>
              <li>
                <div class="list-container">
                  <nuxt-link :to="{ path: '/company/the-leader-in-supply-chain-management-edgistify', hash: '#our-advisors' }"
                    style="text-decoration: none; color: inherit">
                    Mentors
                  </nuxt-link>
                </div>
              </li>
              <li>
                <div class="list-container">
                  <nuxt-link :to="{ path: '/company/the-leader-in-supply-chain-management-edgistify', hash: '#our-team' }" style="text-decoration: none; color: inherit">
                    Team
                  </nuxt-link>
                </div>
              </li>
              <li>
                <div class="list-container">
                  <nuxt-link :to="{ path: '/careers/exciting-opportunities-join-the-team-edgistify', hash: '#careers-container' }"
                    style="text-decoration: none; color: inherit">
                    Careers
                  </nuxt-link>
                </div>
              </li>
              <li>
                <div class="list-container">Contact Us</div>
              </li>
              <li>
                <div class="list-container">
                  <nuxt-link :to="{ path: '/resources/access-the-tools-you-need-to-learn-resources-edgistify' }" style="text-decoration: none; color: inherit">
                    Newsroom
                  </nuxt-link>
                </div>
              </li>
              <li>
                <div class="list-container">
                  <nuxt-link :to="{ path: '/resources/access-the-tools-you-need-to-learn-resources-edgistify', hash: '#resource-media' }"
                    style="text-decoration: none; color: inherit">
                    Awards
                  </nuxt-link>
                </div>
              </li>
              <!-- <li>
                <div class="list-container">Design</div>
              </li> -->
              <li>
                <div class="list-container">
                  <nuxt-link :to="{ path: '/resources/access-the-tools-you-need-to-learn-resources-edgistify', hash: '#resource-media' }"
                    style="text-decoration: none; color: inherit">
                    Media and Mentions
                  </nuxt-link>
                </div>
              </li>
            </ul>
          </v-col>
          <v-col class="social-media-link-container px-0">
            <ul>
              <li>Follow Us</li>
              <li>
                <a href="https://in.linkedin.com/company/edgistify" target="_blank"><font-awesome-icon
                    :icon="['fab', 'linkedin']" class="icon" /></a>
                <a href="https://www.instagram.com/edgistify/?hl=en" target="_blank"><font-awesome-icon
                    :icon="['fab', 'square-instagram']" class="icon" /></a>
                <a href="https://www.facebook.com/edgistify/" target="_blank"><font-awesome-icon
                    :icon="['fab', 'square-facebook']" class="icon" /></a>
              </li>
              <li>
                <a href="https://twitter.com/edgistify?lang=en" target="_blank"><font-awesome-icon
                    :icon="['fab', 'twitter']" class="icon" /></a>
                <a href="https://www.youtube.com/c/Edgistify" target="_blank"><font-awesome-icon
                    :icon="['fab', 'youtube']" class="icon" /></a>
              </li>
            </ul>
            <v-col class="help-container px-0">

              <nuxt-link
                :to="{
                  path: '/Privacy',
                }"
                @click.native="scrollToLocation"
                style="text-decoration: none; color: inherit"
              >
              <span>Privacy Policy</span>

              </nuxt-link>

              <nuxt-link
                :to="{
                  path: '/Terms',
                }"
                @click.native="scrollToLocation"
                style="text-decoration: none; color: inherit"
              >
              <span>Terms and Conditions</span>

              </nuxt-link>
              <nuxt-link
                :to="{
                  path: '/Sitemap',
                }"
                @click.native="scrollToLocation"
                style="text-decoration: none; color: inherit"
              >
              <span>Sitemap</span>

              </nuxt-link>            </v-col>
          </v-col>
        </v-col>
      </v-col>
    </v-row>
    <v-col class="footer-text">
      <span>© 2023 OptiSupply Chain Solution Pvt Ltd | All Rights Reserved</span>
    </v-col>
  </v-container>
</template>
<script>
import ConnectModal from "../ModalForm/ConnectModal.vue";

export default {
  components: {
    ConnectModal,
  },
  data () {
    return {
      isDevice: false,
      showModal: false,
    };
  },
  methods: {},
  mounted () {
    if (window.innerWidth < 850) {
      this.isDevice = true;
    } else {
      this.isDevice = false;
    }
  },
};
</script>
<style lang="scss" scoped>
.footer-container {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: auto;
  align-items: center;
  justify-content: center;

  .footer-content {
    display: flex;
    width: 100%;
    height: 100%;
    background-color: #0c0c0c;
    // background-image: url("/Common/footer-background-grid.png");
    background-size: contain;
    background-position-x: right;

    .logo-container {
      display: flex;
      width: 50%;
      height: 100%;
      padding: 0 6%;
      transition: all 0.5s ease;

      h1 {
        margin-top: 5.5%;
        width: 200px;
        font-size: 4.5rem;
        color: #ffffff;

        font-family: "Outfit";

        &:hover {
          span {
            color: #00a699;
          }
        }
      }
    }

    .content-container {
      font-family: "outfit";
      display: flex;
      padding: 0 6%;
      flex-direction: column;
      justify-content: flex-end;
      align-items: flex-end;
      font-size: 14px;
      margin-top: 2rem;

      .page-link-container,
      .refrence-link-container {
        ul {
          width: 170%;

          li {
            background-image: none;
            margin: 4px;
            width: max-content;
            display: flex;
            color: #ffffff;

            // justify-content: space-around;
            // padding-right: 1rem;
            .list-container {
              display: flex;
              align-items: center;
              justify-content: space-between;
              padding-left: 1.5rem;

              .img-container {
                width: 40%;

                .img {
                  width: 1.5rem;
                  height: 1.5rem;
                }
              }

              .txt-container {
                width: 60%;
              }
            }
          }

          li:hover {
            background-image: url("/green-forward-arrow.png");
            height: 70%;
            background-position-x: -4px;
            background-position-y: -4px;
          }
        }
      }

      ul {
        list-style-type: none;
        cursor: pointer;
        transition: all 0.3s ease;

        li {
          &:hover {
            color: #00a699;
          }
        }
      }

      .links-container {
        display: flex;
        width: 100%;
        height: 60%;
        padding-right: 0;
        justify-content: space-evenly;

        .social-media-link-container {
          padding-right: 0;
          ul {
            float: right;
            li {
              &:hover {
                color: white;
              }

              margin-top: 5px;
              color: #ffffff;

              a {
                color: white !important;
              }

              svg {
                width: 18px;
                height: 18px;
                margin: 0 3px;
              }

              .icon:hover {
                color: #00a699;
              }
            }
          }
        }
      }

      .news-letter-signup-container {
        font-family: "Noto Serif";
        display: flex;
        width: 100%;
        height: 30%;
        flex-direction: column;
        padding-left: 5rem;
        padding-right: 0 !important;
        // padding-right: 3px;
        color: #ffffff;

        .input-container {
          margin-top: 1rem;
          display: flex;
        }
      }

      .help-container {
        display: flex;
        width: 86%;
        // padding-bottom: 25px;
        align-items: center;
        justify-content: space-between;
        transition: all 0.3s ease;
        // padding-left: 95px;
        color: #ffffff;

        span {
          cursor: pointer;

          &:hover {
            color: #00a699;
          }
        }
      }
    }
  }

  .footer-text {
    display: flex;
    width: 100%;
    height: 10%;
    height: 45px;
    padding: 0 6%;
    border-top: 1px solid #00a699;
    background-color: #0c0c0c;

    span {
      margin-top: 1%;
      font-size: 12px;
      color: #00a699;
    }
  }
}

@media (max-width: 850px) {

  .social-media-link-container {
    margin-top: -48px !important;
    padding-top: 0 !important;
    ul {
    float: unset !important;
  }}
  .footer-container {
    display: flex !important;
    flex-direction: column !important;
    width: 100% !important;
    height: auto !important;

    .footer-content {
      flex-direction: column !important;
      align-items: flex-start !important;
      background-image: none !important;

      .logo-container {
        padding: 0 6% !important;
        width: 100% !important;

        h1 {
          margin-top: 0rem !important;
          // width: 100% !important;
          font-size: 4.5rem !important;
          padding: 0 !important;
        }
        span {
            color: #00a699;
          }
      }

      .content-container {
        width: 100% !important;
        margin-top: 2rem !important;
        padding: 0 6% !important;

        .news-letter-signup-container {
          height: 25% !important;
          // padding-left: 2rem !important;

          span {
            font-size: 18px !important;
            font-weight: 300 !important;
            line-height: 0.938rem !important;
          }

          .input-container {
            margin-top: 0 !important;
            width: 100% !important;
            height: 4.409rem !important;
          }
        }

        .links-container {
          height: 100% !important;
          justify-content: flex-end !important;
          align-items: center !important;
          gap: 17% !important;

          ul {
            li {
              font-size: 0.875rem !important;
              line-height: 18px !important;
              font-weight: 300 !important;
              margin-top: 0.65rem !important;
            }
          }

          .page-link-container {
            // padding-right: 10rem !important;

            ul {
              width: max-content !important;
              padding-left: 0% !important;

              li {
                background-image: none !important;

               

                &:hover {
                  background-image: url("/green-forward-arrow.png") !important;
                  background-position-x: 4px !important;
                  background-position-y: -6px !important;
                }
              }
            }
          }

          .social-media-link-container {
            padding-top: 3rem;

            ul {
              padding-left: 0 !important;

              li {
                margin-top: 0.75rem !important;
              }
            }

            .help-container {
              height: 30% !important;
              flex-direction: column !important;
              padding-top: 2.5rem !important;
              align-items: flex-start !important;
              color: #ffffff !important;
              font-family: "Outfit" !important;
              font-style: normal !important;
              font-weight: 300 !important;
              font-size: 0.875rem !important;
              line-height: 20px !important;
              padding-left: 0rem !important;

              span {
                width: max-content !important;
              }
            }
          }
        }
      }
    }

    .footer-text {
      padding: 0 2rem !important;

      span {
        padding: 0 !important;
        font-size: 0.69rem !important;
      }
    }
  }
}
</style>
