<template>
  <div class="header-container">
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <div class="mob-container">
      <div class="header">
        <div class="logo-container">
          <nuxt-link to="/">
            <v-img
              alt="Edgistify"
              src="/Edgistify.png"
              style="height: 35px"
              class="logo"
              contain
            >
            </v-img>
          </nuxt-link>
        </div>
        <div class="menu-container" @click="toggleMenu">
          <v-img
            src="/hamburger-icon.png"
            class="img"
            contain
            v-if="!isMenuOpen"
          >
          </v-img>
          <v-img src="/close-icon-white.png" class="img" contain v-else>
          </v-img>
        </div>
      </div>
      <div class="mob-dropdown" v-bind:class="{ show: isMenuOpen }">
        <div class="mob-dropdown-container">
          <ul class="menu-container-mob">
            <li
              class="menu-item"
              :class="{ selected: toggleTab === 'Solutions' && showDropdown }"
              @click="() => onToggleDropdown('Solutions')"
            >
              <div class="container">
                <div class="title">Solutions</div>
                <ul class="options" v-if="toggleTab === 'Solutions'">
                  <li
                    class="sub-options"
                    @click="() => toggleSecondaryMenu('Warehouse')"
                  >
                    <div class="sub-options-wrapper">
                      <div class="option-label">Warehousing</div>
                      <div class="options-icon">
                        <v-img src="/forward-arrow.png" class="img" contain>
                        </v-img>
                      </div>
                    </div>
                  </li>
                  <li
                    class="sub-options"
                    @click="() => toggleSecondaryMenu('Same Day Delivery')"
                  >
                    <div class="sub-options-wrapper">
                      <div class="option-label">Same Day Delivery</div>
                      <div class="options-icon">
                        <v-img src="/forward-arrow.png" class="img" contain>
                        </v-img>
                      </div>
                    </div>
                  </li>
                  <li
                    class="sub-options"
                    @click="() => toggleSecondaryMenu('Technology')"
                  >
                    <div class="sub-options-wrapper">
                      <div class="option-label">Technology</div>
                      <div class="options-icon">
                        <v-img src="/forward-arrow.png" class="img" contain>
                        </v-img>
                      </div>
                    </div>
                  </li>
                  <li
                    class="sub-options"
                    @click="() => toggleSecondaryMenu('Consulting')"
                  >
                    <div class="sub-options-wrapper">
                      <div class="option-label">Consulting</div>
                      <div class="options-icon">
                        <v-img src="/forward-arrow.png" class="img" contain>
                        </v-img>
                      </div>
                    </div>
                  </li>
                  <li
                    class="sub-options"
                    @click="() => toggleSecondaryMenu('Transportation')"
                  >
                    <div class="sub-options-wrapper">
                      <div class="option-label">Transportation</div>
                      <div class="options-icon">
                        <v-img src="/forward-arrow.png" class="img" contain>
                        </v-img>
                      </div>
                    </div>
                  </li>
                  <li
                    class="sub-options"
                    @click="() => toggleSecondaryMenu('Support Services')"
                  >
                    <div class="sub-options-wrapper">
                      <div class="option-label">Support Services</div>
                      <div class="options-icon">
                        <v-img src="/forward-arrow.png" class="img" contain>
                        </v-img>
                      </div>
                    </div>
                  </li>
                </ul>
              </div>
            </li>
            <li class="menu-item">
              <div class="container">
                <div class="title">
                  <nuxt-link
                    :to="{
                      path: '/company/the-leader-in-supply-chain-management-edgistify',
                      hash: '#careers-container',
                    }"
                    @click.native="scrollToLocation"
                    style="text-decoration: none !important; color: inherit"
                  >
                    Company
                  </nuxt-link>
                </div>
              </div>
            </li>
            <li class="menu-item">
              <div class="container">
                <div class="title">
                  <li class="sub-options">
                    <nuxt-link
                      :to="{
                        path: '/resources/access-the-tools-you-need-to-learn-resources-edgistify',
                        hash: '#resource-blog',
                      }"
                      @click.native="scrollToLocation"
                      style="text-decoration: none !important; color: inherit"
                    >
                      Resources
                    </nuxt-link>
                  </li>
                </div>
              </div>
            </li>
            <li class="menu-item">
              <div class="container">
                <div class="title">
                  <nuxt-link
                    :to="{
                      path: '/careers/exciting-opportunities-join-the-team-edgistify',
                      hash: '#careers-container',
                    }"
                    @click.native="scrollToLocation"
                    style="text-decoration: none !important; color: inherit"
                  >
                    Careers
                  </nuxt-link>
                </div>
              </div>
            </li>
          </ul>
          <v-btn
            class="contact-us button primary"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="1000"
            @click="showModal = true"
          >
            Contact Us
          </v-btn>
        </div>
      </div>
      <div class="mob-dropdown" v-bind:class="{ show: isSecondaryMenuOpen }">
        <div class="mob-secondary-options">
          <div class="back-container">
            <div class="back-options-icon">
              <v-img src="/backward-arrow.png" class="img" contain> </v-img>
            </div>
            <div class="back-title" @click="goBack">Back</div>
          </div>
          <div class="secondary-options-title">Solutions</div>
        </div>
        <ul class="mob-options">
          <li class="sub-options-secondary">
            <div
              class="secondary-list"
              @mouseenter="() => toggleSubList('warehouse')"
            >
              <div class="list-label">Warehousing</div>
              <div class="list-icon">
                <v-img src="/forward-arrow.png" class="img" contain> </v-img>
              </div>
            </div>
            <ul
              class="sublist-options"
              v-if="subListMenu === 'warehouse' || selectedMenu === 'Warehouse'"
            >
              <li class="sublist">
                <nuxt-link
                  :to="{
                    path: '/solutions/warehouse-efficient-storage-and-management-solutions-edgistify',
                    hash: '#warehouse-container',
                  }"
                  @click.native="scrollToLocation"
                  style="text-decoration: none !important; color: inherit"
                >
                  E-commerce Fulfillment
                </nuxt-link>
              </li>
              <li class="sublist">
                <nuxt-link
                  :to="{
                    path: '/solutions/warehouse-efficient-storage-and-management-solutions-edgistify',
                    hash: '#dark_store',
                  }"
                  @click.native="scrollToLocation"
                  style="text-decoration: none !important; color: inherit"
                >
                  Dark Store Operations
                </nuxt-link>
              </li>
              <li class="sublist">
                <nuxt-link
                  :to="{
                    path: '/solutions/warehouse-efficient-storage-and-management-solutions-edgistify',
                    hash: '#b2b_retail',
                  }"
                  @click.native="scrollToLocation"
                  style="text-decoration: none !important; color: inherit"
                >
                  B2B Retail Distribution
                </nuxt-link>
              </li>
            </ul>
          </li>
          <li class="sub-options-secondary">
            <div
              class="secondary-list"
              @mouseenter="() => toggleSubList('samedaydelivery')"
            >
              <div class="list-label">Same Day Delivery</div>
              <div class="list-icon">
                <v-img src="/forward-arrow.png" class="img" contain> </v-img>
              </div>
            </div>
            <ul
              class="sublist-options"
              v-if="
                subListMenu === 'samedaydelivery' ||
                selectedMenu === 'Same Day Delivery'
              "
            >
              <li class="sublist">
                <nuxt-link
                  :to="{
                    path: '/solutions/same-day-delivery-fast-reliable-and-convenient-edgistify',
                    hash: '#olutions-sameday-container',
                  }"
                  @click.native="scrollToLocation"
                  style="text-decoration: none !important; color: inherit"
                >
                  D2C Brands
                </nuxt-link>
              </li>
              <li class="sublist">
                <nuxt-link
                  :to="{
                    path: '/solutions/same-day-delivery-fast-reliable-and-convenient-edgistify',
                    hash: '#ebrands',
                  }"
                  @click.native="scrollToLocation"
                  style="text-decoration: none !important; color: inherit"
                >
                  Legacy Brands
                </nuxt-link>
              </li>
              <li class="sublist">
                <nuxt-link
                  :to="{
                    path: '/solutions/same-day-delivery-fast-reliable-and-convenient-edgistify',
                    hash: '#ecommerce',
                  }"
                  @click.native="scrollToLocation"
                  style="text-decoration: none !important; color: inherit"
                >
                  E-commerce Brands
                </nuxt-link>
              </li>
            </ul>
          </li>
          <li class="sub-options-secondary">
            <div
              class="secondary-list"
              @mouseenter="() => toggleSubList('technology')"
            >
              <div class="list-label">Technology</div>
              <div class="list-icon">
                <v-img src="/forward-arrow.png" class="img" contain> </v-img>
              </div>
            </div>
            <ul
              class="sublist-options"
              v-if="
                subListMenu === 'technology' || selectedMenu === 'Technology'
              "
            >
              <li class="sublist">
                <nuxt-link
                  :to="{
                    path: '/solutions/tech-driven-supply-chain-and-warehouse-management-edgistify',
                    hash: '#solutions-technology-container',
                  }"
                  @click.native="scrollToLocation"
                  style="text-decoration: none !important; color: inherit"
                >
                  Order Management System
                </nuxt-link>
              </li>
              <li class="sublist">
                <nuxt-link
                  :to="{
                    path: '/solutions/tech-driven-supply-chain-and-warehouse-management-edgistify',
                    hash: '#wms',
                  }"
                  @click.native="scrollToLocation"
                  style="text-decoration: none !important; color: inherit"
                >
                  Warehouse Management System
                </nuxt-link>
              </li>
              <li class="sublist">
                <nuxt-link
                  :to="{
                    path: '/solutions/tech-driven-supply-chain-and-warehouse-management-edgistify',
                    hash: '#fms',
                  }"
                  @click.native="scrollToLocation"
                  style="text-decoration: none !important; color: inherit"
                >
                  Integrations
                </nuxt-link>
              </li>
            </ul>
          </li>
          <li class="sub-options-secondary">
            <div
              class="secondary-list"
              @mouseenter="() => toggleSubList('consulting')"
            >
              <div class="list-label">Consulting</div>
              <div class="list-icon">
                <v-img src="/forward-arrow.png" class="img" contain> </v-img>
              </div>
            </div>
            <ul
              class="sublist-options"
              v-if="
                subListMenu === 'consulting' || selectedMenu === 'Consulting'
              "
            >
              <li class="sublist">
                <nuxt-link
                  :to="{
                    path: '/solutions/maximizing-efficiency-and-reducing-costs-consulting-of-supply-chain-management-edgistify',
                    hash: '#fms',
                  }"
                  @click.native="scrollToLocation"
                  style="text-decoration: none !important; color: inherit"
                >
                  Supply Chain Process Development
                </nuxt-link>
              </li>
              <li class="sublist">
                <nuxt-link
                  :to="{
                    path: '/solutions/maximizing-efficiency-and-reducing-costs-consulting-of-supply-chain-management-edgistify',
                    hash: '#solutions-supportservices-container',
                  }"
                  @click.native="scrollToLocation"
                  style="text-decoration: none !important; color: inherit"
                >
                  Network Planning and Optimization
                </nuxt-link>
              </li>
              <li class="sublist">
                <nuxt-link
                  :to="{
                    path: '/solutions/tech-driven-supply-chain-and-warehouse-management-edgistify',
                    hash: '#fms',
                  }"
                  @click.native="scrollToLocation"
                  style="text-decoration: none !important; color: inherit"
                >
                  KPI Development and Benchmarking
                </nuxt-link>
              </li>
            </ul>
          </li>
          <li class="sub-options-secondary">
            <div
              class="secondary-list"
              @mouseenter="() => toggleSubList('transportation')"
            >
              <div class="list-label">Transportation</div>
              <div class="list-icon">
                <v-img src="/forward-arrow.png" class="img" contain> </v-img>
              </div>
            </div>
            <ul
              class="sublist-options"
              v-if="
                subListMenu === 'transportation' ||
                selectedMenu === 'Transportation'
              "
            >
              <li class="sublist">
                <nuxt-link
                  :to="{
                    path: '/solutions/edgitify-logistics-channel-for-warehousing-and-transportation-streamline-your-operations',
                    hash: '#solutions-transportation-container',
                  }"
                  @click.native="scrollToLocation"
                  style="text-decoration: none !important; color: inherit"
                >
                  First Mile
                </nuxt-link>
              </li>
              <li class="sublist">
                <nuxt-link
                  :to="{
                    path: '/solutions/edgitify-logistics-channel-for-warehousing-and-transportation-streamline-your-operations',
                    hash: '#middle-mile',
                  }"
                  @click.native="scrollToLocation"
                  style="text-decoration: none !important; color: inherit"
                >
                  Middle Mile
                </nuxt-link>
              </li>
              <li class="sublist">
                <nuxt-link
                  :to="{
                    path: '/solutions/edgitify-logistics-channel-for-warehousing-and-transportation-streamline-your-operations',
                    hash: '#last-mile',
                  }"
                  @click.native="scrollToLocation"
                  style="text-decoration: none !important; color: inherit"
                >
                  Last Mile
                </nuxt-link>
              </li>
            </ul>
          </li>
          <li class="sub-options-secondary">
            <div
              class="secondary-list"
              @mouseenter="() => toggleSubList('supportservices')"
            >
              <div class="list-label">Support Services</div>
              <div class="list-icon">
                <v-img src="/forward-arrow.png" class="img" contain> </v-img>
              </div>
            </div>
            <ul
              class="sublist-options"
              v-if="
                subListMenu === 'supportservices' ||
                selectedMenu === 'Support Services'
              "
            >
              <li class="sublist">
                <nuxt-link
                  :to="{
                    path: '/solutions/support-services-for-supply-chain-optimization-and-management-ensure-success-edgistify',
                    hash: '#solutions-supportservices-container',
                  }"
                  @click.native="scrollToLocation"
                  style="text-decoration: none !important; color: inherit"
                >
                  Warehouse Space
                </nuxt-link>
              </li>
              <li class="sublist">
                <nuxt-link
                  :to="{
                    path: '/solutions/support-services-for-supply-chain-optimization-and-management-ensure-success-edgistify',
                    hash: '#warehouse-infra',
                  }"
                  @click.native="scrollToLocation"
                  style="text-decoration: none !important; color: inherit"
                >
                  Warehouse Infra
                </nuxt-link>
              </li>
              <li class="sublist">
                <nuxt-link
                  :to="{
                    path: '/solutions/support-services-for-supply-chain-optimization-and-management-ensure-success-edgistify',
                    hash: '#manpower',
                  }"
                  @click.native="scrollToLocation"
                  style="text-decoration: none !important; color: inherit"
                >
                  Manpower
                </nuxt-link>
              </li>
            </ul>
          </li>
        </ul>
        <v-btn
          class="contact-us button primary"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="1000"
          @click="showModal = true"
          style="margin-left: 30% !important"
        >
          Contact Us
        </v-btn>
      </div>
    </div>
  </div>
</template>

<script>
import ConnectModal from "../ModalForm/ConnectModal.vue";

export default {
  components: {
    ConnectModal,
  },
  data() {
    return {
      isMenuOpen: false,
      showDropdown: true,
      toggleTab: "Solutions",
      isSecondaryMenuOpen: false,
      selectedMenu: "",
      subListMenu: "",
      showModal: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
      this.isSecondaryMenuOpen = false;
    },
    onToggleDropdown(tab) {
      if (this.showDropdown) {
        if (this.toggleTab === tab) {
          this.showDropdown = false;
        } else {
          this.toggleTab = tab;
        }
      } else {
        this.showDropdown = true;
        this.toggleTab = tab;
      }
    },
    toggleSecondaryMenu(opt) {
      this.isSecondaryMenuOpen = !this.isSecondaryMenuOpen;
      this.selectedMenu = opt;
      console.log(this.selectedMenu, "this.selectedMenu");
    },
    toggleSubList(options) {
      this.subListMenu = options;
      this.selectedMenu = "";
    },
    goBack() {
      this.isSecondaryMenuOpen = false;
      this.selectedMenu = "";
      this.subListMenu = "";
    },
    scrollToLocation() {
      if (this.$route.hash) {
        this.isSecondaryMenuOpen = false;
        this.isMenuOpen = false;
        this.goBack();
        const anchor = document.querySelector(`${this.$route.hash}`);
        if (anchor) {
          window.scrollTo({
            top: anchor.getBoundingClientRect().top + window.pageYOffset,
          });
        }
      }
    },
  },
};
</script>

<style lang="scss" scoped>
@media (max-width: 850px) {
  .contact-us {
    width: 10.313rem !important;
    height: 3rem !important;
    background: #00a699 !important;
    border-radius: 4.5rem !important;
    font-family: "Noto Serif" !important;
    font-style: normal !important;
    font-weight: 700 !important;
    font-size: 18px !important;
    line-height: 25px !important;

    &.button {
      display: flex !important;
      text-transform: capitalize !important;
      height: 42px !important;
      position: fixed;
      bottom: 150px;

      align-items: center !important;
      justify-content: center !important;
      border: 1px solid #00a699 !important;
      border-radius: 40px !important;
      color: #fff !important;
      padding: 10px 40px !important;
      font-family: "Noto Serif" !important;
      font-style: normal !important;
      font-weight: 500 !important;

      &.primary {
        background-color: #00a699 !important;
        box-shadow: inset 0 0 0 0 #00a699 !important;
        transition: color 0.3s ease-in-out, box-shadow 0.3s ease-in-out !important;

        &:hover {
          box-shadow: inset 206px 0 0 0 #ffffff !important;
          color: #000000 !important;
        }
      }

      &.secondry {
        border: 2px solid #fff !important;
        background-color: transparent !important;
        margin-left: 72px !important;

        &:hover {
          border-color: #008b80 !important;
        }

        &.clicked {
          border-color: #008b80 !important;
          color: #008b80 !important;
        }

        b {
          font-family: "Outfit" !important;
        }
      }
    }
  }
  .header-container {
    display: flex !important;
    width: 100% !important;
    height: 4.688rem !important;

    .mob-container {
      height: 100% !important;
      width: 100% !important;

      .header {
        display: flex !important;
        align-items: center !important;
        position: fixed !important;
        z-index: 3 !important;
        width: 100% !important;
        padding: 0 !important;
        justify-content: space-between !important;
        background: #000000 !important;

        .logo-container {
          display: flex !important;
          width: 2.823rem !important;
          height: 4.688rem !important;
          align-items: center !important;

          .logo {
            color: #008b80 !important;
            font-family: "Outfit" !important;
            //   width: 4.823rem !important;
            //   height: 7.188rem !important;
          }
        }

        .menu-container {
          display: flex !important;
          margin-right: 1rem !important;
        }
      }

      .mob-dropdown.show {
        position: fixed !important;
        z-index: 3 !important;
        background: #101010 !important;
        top: 4rem !important;
        width: 101vw !important;
        height: 100vh !important;
        display: flex !important;
        flex-direction: column !important;

        .mob-dropdown-container {
          height: 100% !important;
          width: 100% !important;
          display: flex !important;
          flex-direction: column !important;
          justify-content: flex-start !important;
          align-items: center !important;
          margin-top: 1rem !important;

          .menu-container-mob {
            display: flex !important;
            flex-direction: column !important;
            align-items: flex-start !important;
            justify-content: center !important;
            position: relative !important;
            width: 100% !important;
            height: auto !important;
            list-style-type: none !important;

            .menu-item {
              font-weight: 300 !important;
              font-size: 1.75rem !important;
              line-height: 2.188rem !important;
              height: auto !important;
              cursor: pointer !important;
              transition: all 0.3s ease !important;
              color: #8d8d8d !important;
              position: relative !important;

              .container {
                display: flex !important;
                flex-direction: column !important;
                width: 100% !important;
                height: auto !important;
                margin-top: 0.25rem !important;
                color: #fff !important;
                padding: 6px 0 !important;

                .options {
                  list-style: none !important;
                  font-family: "Outfit" !important;
                  font-style: normal !important;
                  font-weight: 300 !important;
                  font-size: 1rem !important;
                  line-height: 1.25rem !important;
                  height: auto !important;
                  margin: 1rem !important;
                  color: #ffffff !important;
                  display: flex !important;
                  flex-direction: column !important;
                  align-items: baseline !important;

                  .sub-options {
                    margin-bottom: 0.5rem !important;

                    .sub-options-wrapper {
                      display: flex !important;
                      justify-content: space-evenly !important;
                      align-items: baseline !important;

                      .options-icon {
                        padding-left: 1rem !important;
                      }
                    }
                  }
                }

                .title {
                  display: flex !important;
                  width: 100% !important;
                  height: auto !important;
                  align-items: center !important;
                  user-select: none !important;
                  font-family: "Outfit" !important;
                }
              }
            }
          }
        }

        .mob-secondary-options {
          width: 100vw !important;
          padding: 0 6% !important;
          margin-top: 6%;

          .back-container {
            display: flex !important;
            align-items: baseline !important;

            .back-options-icon {
              padding-right: 1rem !important;
            }

            .back-title {
              font-family: "Outfit" !important;
              font-style: normal !important;
              font-weight: 300 !important;
              font-size: 1rem !important;
              line-height: 1.25rem !important;
              color: #ffffff !important;
              font-family: "Outfit" !important;
            }
          }

          .secondary-options-title {
            font-family: "Outfit" !important;
            font-style: normal !important;
            font-weight: 300 !important;
            font-size: 1.75rem !important;
            line-height: 2.188rem !important;
            color: #ffffff !important;
            font-family: "Outfit" !important;

            padding-top: 12px;
            padding-bottom: 12px;
          }
        }

        .mob-options {
          display: flex !important;
          flex-direction: column !important;
          margin: 0 0 0 6% !important;
          justify-content: space-evenly !important;

          .sub-options-secondary {
            width: 100% !important;
            display: flex !important;
            flex-direction: column !important;
            padding: 6px 0;
            font-family: "Outfit";

            .secondary-list {
              display: flex !important;
              // justify-content: space-evenly !important;
              align-items: baseline !important;

              .list-label {
                font-family: "Outfit" !important;
                font-style: normal !important;
                font-weight: 300 !important;
                font-size: 1rem !important;
                line-height: 1.25rem !important;
                color: #ffffff !important;
              }

              .list-icon {
                padding-left: 1rem !important;
              }
            }

            .sublist-options {
              list-style: none !important;
              display: flex !important;
              flex-direction: column !important;
              padding-left: 1rem !important;
              padding-top: 1rem !important;
              cursor: pointer !important;

              .sublist {
                width: fit-content !important;
                font-family: "Outfit" !important;
                font-style: normal !important;
                font-weight: 300 !important;
                font-size: 0.813rem !important;
                line-height: 1rem !important;
                color: #8d8d8d !important;
                padding-bottom: 1rem !important;
              }

              .sublist:hover {
                color: #ffffff !important;
                cursor: pointer !important;
              }
            }
          }
        }
      }

      .mob-dropdown {
        display: none !important;
      }
    }
  }
}
</style>
