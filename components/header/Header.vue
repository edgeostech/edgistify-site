<template>
  <div>
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <div class="header-container" :class="{ hidden: !showNavbar }" @mouseleave="() => (showDropdown = false)">
      <div class="header">
        <div class="logo-container">
          <nuxt-link to="/">
            <v-img alt="Edgistify" src="/Edgistify.png" height="40px" class="logo" contain>
            </v-img>
          </nuxt-link>
        </div>
        <ul class="menu-container">
          <li class="menu-item" :class="{
            selected: toggleTab === 'Solutions' && showDropdown,
            'active-link': $route.path.startsWith('/solutions/'),
          }" @mouseenter="() => onToggleDropdown('Solutions')">
            <div class="container">
              <div class="title">Solutions</div>
              <div class="dropdown-icon">
                <v-img src="/Common/down-arrow.png" class="img" contain>
                </v-img>
              </div>
            </div>
          </li>
          <li class="menu-item" :class="{
            selected: toggleTab === 'Company' && showDropdown,
            'active-link': $route.path === '/company/the-leader-in-supply-chain-management-edgistify',
          }" @mouseenter="() => onToggleDropdown('Company')">
            <div class="container">
              <div class="title">
                <nuxt-link to="/company/the-leader-in-supply-chain-management-edgistify"
                  style="text-decoration: none; color: inherit">
                  Company
                </nuxt-link>
              </div>
              <div class="dropdown-icon">
                <v-img src="/Common/down-arrow.png" class="img" contain>
                </v-img>
              </div>
            </div>
          </li>
          <li class="menu-item" :class="{
            selected: toggleTab === 'Resources' && showDropdown,
            'active-link': $route.path === '/resources/access-the-tools-you-need-to-learn-resources-edgistify',
          }" @mouseenter="() => onToggleDropdown('Resources')">
            <div class="container">
              <div class="title">
                <nuxt-link to="/resources/access-the-tools-you-need-to-learn-resources-edgistify"
                  style="text-decoration: none; color: inherit">
                  Resources
                </nuxt-link>
              </div>

              <div class="dropdown-icon">
                <v-img src="/Common/down-arrow.png" class="img" contain>
                </v-img>
              </div>
            </div>
          </li>
          <li class="menu-item" :class="{
            selected: toggleTab === 'Careers' && showDropdown,
            'active-link': $route.path === '/careers/exciting-opportunities-join-the-team-edgistify',
          }" @mouseenter="() => onToggleDropdown('Careers')">
            <div class="container">
              <div class="title">
                <nuxt-link to="/careers/exciting-opportunities-join-the-team-edgistify"
                  style="text-decoration: none; color: inherit">
                  Careers
                </nuxt-link>
              </div>
              <div class="dropdown-icon">
                <v-img src="/Common/down-arrow.png" class="img" contain>
                </v-img>
              </div>
            </div>
          </li>
          <!-- <li class="menu-item button primary">
          <b> Contact Us </b>
        </li> -->
        </ul>
        <v-btn class="contact-us button bg-black" data-aos-once="true" data-aos-easing="ease-in" data-aos-duration="1000"
          @click="showModal = true">
          Contact Us
        </v-btn>
      </div>
      <div class="dropdown" :class="{ hidden: !showDropdown }">
        <div class="dropdown-container">
          <div v-if="toggleTab === 'Solutions'" class="container Solution">
            <div class="section one">
              <nuxt-link to="/solutions/warehouse-efficient-storage-and-management-solutions-edgistify"
                style="text-decoration: none; color: inherit">
                <div class="section-heading">
                  <h4>Warehousing</h4>
                </div>
              </nuxt-link>

              <nuxt-link
                :to="{ path: '/solutions/warehouse-efficient-storage-and-management-solutions-edgistify', hash: '#e_commerce' }"
                @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
                <div class="section-content">
                  <div class="icon">
                    <v-img src="/Common/right-arrow.png" class="img" contain>
                    </v-img>
                  </div>
                  <div class="item">E-commerce Fulfillment</div>
                </div>
              </nuxt-link>

              <nuxt-link
                :to="{ path: '/solutions/warehouse-efficient-storage-and-management-solutions-edgistify', hash: '#dark_store' }"
                @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
                <div class="section-content">
                  <div class="icon">
                    <v-img src="/Common/right-arrow.png" class="img" contain>
                    </v-img>
                  </div>
                  <div class="item">Dark Store Operations</div>
                </div>
              </nuxt-link>

              <nuxt-link
                :to="{ path: '/solutions/warehouse-efficient-storage-and-management-solutions-edgistify', hash: '#b2b_retail' }"
                @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
                <div class="section-content">
                  <div class="icon">
                    <v-img src="/Common/right-arrow.png" class="img" contain>
                    </v-img>
                  </div>
                  <div class="item">B2B Retail Distribution</div>
                </div>
              </nuxt-link>
              <nuxt-link
                to="/solutions/maximizing-efficiency-and-reducing-costs-consulting-of-supply-chain-management-edgistify"
                style="text-decoration: none; color: inherit">
                <div class="section-heading second">
                  <h4>Consulting</h4>
                </div>
              </nuxt-link>

              <nuxt-link :to="{
                path: '/solutions/maximizing-efficiency-and-reducing-costs-consulting-of-supply-chain-management-edgistify',
                hash: '#warehouse-space',
              }" @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
                <div class="section-content">
                  <div class="icon">
                    <v-img src="/Common/right-arrow.png" class="img" contain>
                    </v-img>
                  </div>
                  <div class="item">Supply Chain Process Development</div>
                </div>
              </nuxt-link>

              <nuxt-link :to="{
                path: '/solutions/maximizing-efficiency-and-reducing-costs-consulting-of-supply-chain-management-edgistify',
                hash: '#warehouse-space',
              }" @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
                <div class="section-content">
                  <div class="icon">
                    <v-img src="/Common/right-arrow.png" class="img" contain>
                    </v-img>
                  </div>
                  <div class="item">Network Planning and Optimization</div>
                </div>
              </nuxt-link>
              <nuxt-link :to="{
                path: '/solutions/maximizing-efficiency-and-reducing-costs-consulting-of-supply-chain-management-edgistify',
                hash: '#warehouse-space',
              }" @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
                <div class="section-content">
                  <div class="icon">
                    <v-img src="/Common/right-arrow.png" class="img" contain>
                    </v-img>
                  </div>
                  <div class="item">KPI Development and Benchmarking</div>
                </div>
              </nuxt-link>
              <!-- <div class="section-content">
              <div class="icon">
                <v-img src="/Common/right-arrow.png" class="img" contain>
                </v-img>
              </div>
              <div class="item">SupplyChain Consultancy</div>
            </div> -->
            </div>
            <div class="section two">
              <div class="section-heading">
                <nuxt-link to="/solutions/same-day-delivery-fast-reliable-and-convenient-edgistify"
                  style="text-decoration: none; color: inherit">
                  <h4>Same Day Delivery</h4>
                </nuxt-link>
              </div>
              <nuxt-link
                :to="{ path: '/solutions/same-day-delivery-fast-reliable-and-convenient-edgistify', hash: '#dtoc' }"
                @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
                <div class="section-content">
                  <div class="icon">
                    <v-img src="/Common/right-arrow.png" class="img" contain>
                    </v-img>
                  </div>
                  <div class="item">D2C Brands</div>
                </div>
              </nuxt-link>
              <nuxt-link
                :to="{ path: '/solutions/same-day-delivery-fast-reliable-and-convenient-edgistify', hash: '#ebrands' }"
                @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
                <div class="section-content">
                  <div class="icon">
                    <v-img src="/Common/right-arrow.png" class="img" contain>
                    </v-img>
                  </div>
                  <div class="item">Legacy Brands</div>
                </div>
              </nuxt-link>
              <nuxt-link
                :to="{ path: '/solutions/same-day-delivery-fast-reliable-and-convenient-edgistify', hash: '#ecommerce' }"
                @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
                <div class="section-content">
                  <div class="icon">
                    <v-img src="/Common/right-arrow.png" class="img" contain>
                    </v-img>
                  </div>
                  <div class="item">Ecommerce Brands</div>
                </div>
              </nuxt-link>
              <div class="section-heading second">
                <nuxt-link
                  to="/solutions/support-services-for-supply-chain-optimization-and-management-ensure-success-edgistify"
                  style="text-decoration: none; color: inherit">
                  <h4>Support Services</h4>
                </nuxt-link>
              </div>
              <nuxt-link :to="{
                path: '/solutions/support-services-for-supply-chain-optimization-and-management-ensure-success-edgistify',
                hash: '#warehouse-space',
              }" @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
                <div class="section-content">
                  <div class="icon">
                    <v-img src="/Common/right-arrow.png" class="img" contain>
                    </v-img>
                  </div>
                  <div class="item">Warehouse Space</div>
                </div>
              </nuxt-link>
              <nuxt-link :to="{
                path: '/solutions/support-services-for-supply-chain-optimization-and-management-ensure-success-edgistify',
                hash: '#warehouse-infra',
              }" @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
                <div class="section-content">
                  <div class="icon">
                    <v-img src="/Common/right-arrow.png" class="img" contain>
                    </v-img>
                  </div>
                  <div class="item">Warehouse Infra</div>
                </div>
              </nuxt-link>
              <nuxt-link
                :to="{ path: '/solutions/support-services-for-supply-chain-optimization-and-management-ensure-success-edgistify', hash: '#manpower' }"
                @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
                <div class="section-content">
                  <div class="icon">
                    <v-img src="/Common/right-arrow.png" class="img" contain>
                    </v-img>
                  </div>
                  <div class="item">Manpower</div>
                </div>
              </nuxt-link>
            </div>
            <div class="section three">
              <div class="section-heading">
                <nuxt-link to="/solutions/tech-driven-supply-chain-and-warehouse-management-edgistify"
                  style="text-decoration: none; color: inherit">
                  <h4>Technology</h4>
                </nuxt-link>
              </div>
              <nuxt-link
                :to="{ path: '/solutions/tech-driven-supply-chain-and-warehouse-management-edgistify', hash: '#oms' }"
                @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
                <div class="section-content">
                  <div class="icon">
                    <v-img src="/Common/right-arrow.png" class="img" contain>
                    </v-img>
                  </div>
                  <div class="item">Order Management System</div>
                </div>
              </nuxt-link>
              <nuxt-link
                :to="{ path: '/solutions/tech-driven-supply-chain-and-warehouse-management-edgistify', hash: '#wms' }"
                @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
                <div class="section-content">
                  <div class="icon">
                    <v-img src="/Common/right-arrow.png" class="img" contain>
                    </v-img>
                  </div>
                  <div class="item">Warehouse Management System</div>
                </div>
              </nuxt-link>
              <nuxt-link
                :to="{ path: '/solutions/tech-driven-supply-chain-and-warehouse-management-edgistify', hash: '#fms' }"
                @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
                <div class="section-content">
                  <div class="icon">
                    <v-img src="/Common/right-arrow.png" class="img" contain>
                    </v-img>
                  </div>
                  <div class="item">Integrations</div>
                </div>
              </nuxt-link>
              <div class="section-heading second">
                <nuxt-link
                  to="/solutions/edgitify-logistics-channel-for-warehousing-and-transportation-streamline-your-operations"
                  style="text-decoration: none; color: inherit">
                  <h4>Transportation</h4>
                </nuxt-link>
              </div>
              <nuxt-link
                :to="{ path: '/solutions/edgitify-logistics-channel-for-warehousing-and-transportation-streamline-your-operations', hash: '#first-mile' }"
                @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
                <div class="section-content">
                  <div class="icon">
                    <v-img src="/Common/right-arrow.png" class="img" contain>
                    </v-img>
                  </div>
                  <div class="item">First Mile</div>
                </div>
              </nuxt-link>
              <nuxt-link :to="{
                path: '/solutions/edgitify-logistics-channel-for-warehousing-and-transportation-streamline-your-operations',
                hash: '#middle-mile',
              }" @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
                <div class="section-content">
                  <div class="icon">
                    <v-img src="/Common/right-arrow.png" class="img" contain>
                    </v-img>
                  </div>
                  <div class="item">Middle Mile</div>
                </div>
              </nuxt-link>
              <nuxt-link
                :to="{ path: '/solutions/edgitify-logistics-channel-for-warehousing-and-transportation-streamline-your-operations', hash: '#last-mile' }"
                @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
                <div class="section-content">
                  <div class="icon">
                    <v-img src="/Common/right-arrow.png" class="img" contain>
                    </v-img>
                  </div>
                  <div class="item">Last Mile</div>
                </div>
              </nuxt-link>
            </div>
          </div>
          <div v-if="toggleTab === 'Company'" class="container">
            <nuxt-link
              :to="{ path: '/company/the-leader-in-supply-chain-management-edgistify', hash: '#company-aboutus' }"
              @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
              <div class="menu-item">About Us</div>
            </nuxt-link>
            <nuxt-link :to="{ path: '/company/the-leader-in-supply-chain-management-edgistify', hash: '#our-journey' }"
              @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
              <div class="menu-item">History</div>
            </nuxt-link>
            <nuxt-link :to="{ path: '/company/the-leader-in-supply-chain-management-edgistify', hash: '#vision' }"
              @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
              <div class="menu-item">Vision</div>
            </nuxt-link>
            <nuxt-link :to="{ path: '/company/the-leader-in-supply-chain-management-edgistify', hash: '#our-advisors' }"
              @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
              <div class="menu-item">Mentors</div>
            </nuxt-link>
            <nuxt-link :to="{ path: '/company/the-leader-in-supply-chain-management-edgistify', hash: '#our-founders' }"
              @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
              <div class="menu-item">Founders</div>
            </nuxt-link>
            <nuxt-link :to="{ path: '/company/the-leader-in-supply-chain-management-edgistify', hash: '#our-team' }"
              @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
              <div class="menu-item">Team</div>
            </nuxt-link>
          </div>
          <div v-if="toggleTab === 'Resources'" class="container">
            <nuxt-link
              :to="{ path: '/resources/access-the-tools-you-need-to-learn-resources-edgistify', hash: '#resource-blog' }"
              @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
              <div class="menu-item">Blog</div>
            </nuxt-link>
            <nuxt-link
              :to="{ path: '/resources/access-the-tools-you-need-to-learn-resources-edgistify', hash: '#resource-media' }"
              @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
              <div class="menu-item">Media</div>
            </nuxt-link>
            <nuxt-link
              :to="{ path: '/resources/access-the-tools-you-need-to-learn-resources-edgistify', hash: '#resource-Case-studies' }"
              @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
              <div class="menu-item">Case studies</div>
            </nuxt-link>
            <nuxt-link
              :to="{ path: '/resources/access-the-tools-you-need-to-learn-resources-edgistify', hash: '#resource-Videos' }"
              @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
              <div class="menu-item">Videos</div>
            </nuxt-link>
            <!-- <div class="menu-item">Design</div> -->
          </div>
          <div v-if="toggleTab === 'Careers'" class="container">
            <nuxt-link :to="{ path: '/careers/exciting-opportunities-join-the-team-edgistify', hash: '#careers-joinus' }"
              @click.native="scrollToLocation" style="text-decoration: none; color: inherit">
              <div class="menu-item">Why Join Us</div>
            </nuxt-link>
            <nuxt-link
              :to="{ path: '/careers/exciting-opportunities-join-the-team-edgistify', hash: '#careers-openposition' }"
              @click.native="scrollToLocation"
              style="text-decoration: none; color: inherit"
            >
              <div class="menu-item">Open Positions</div>
            </nuxt-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.header-container {
  position: fixed !important;
  // top: 0;
  display: flex;
  width: 100%;
  height: fit-content;
  flex-direction: column;
  justify-content: space-between;
  // position: relative;
  transition: 0.3s all ease-out;
  transform: translate3d(0, 0, 0);
  z-index: 3;

  .header {
    display: flex;
    align-items: center;
    height: 92px;
    padding: 0 6%;
    justify-content: space-between;
    background-color: #000;

    .logo-container {
      display: flex;

      .logo {
        display: yes;
      }
    }

    .contact-us {
      width: 10.313rem;
      height: 3rem;
      background: #00a699;
      border-radius: 4.5rem;
      font-family: "Noto Serif";
      font-style: normal;
      font-weight: 700;
      font-size: 18px;
      line-height: 25px;

      &.button {
        display: flex;
        text-transform: capitalize;
        height: 42px;
        align-items: center;
        justify-content: center;
        border: 1px solid #00a699;
        border-radius: 40px;
        color: #fff;
        padding: 10px 40px;
        font-family: "Noto Serif";
        font-style: normal;
        font-weight: 500;

        &.primary {
          background-color: #00a699;
          box-shadow: inset 0 0 0 0 #00a699;
          transition: color 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
          margin-left: 100px;

          &:hover {
            box-shadow: inset 206px 0 0 0 #ffffff;
            color: #000000;
          }
        }

        &.secondry {
          border: 2px solid #fff;
          background-color: transparent;
          margin-left: 72px;

          &:hover {
            border-color: #008b80;
          }

          &.clicked {
            border-color: #008b80;
            color: #008b80;
          }

          b {
            font-family: "Outfit";
          }
        }
      }
    }
  }

  .dropdown {
    //height: calc(100vh - 98px);
    background: #00000099;
    z-index: 2;
    color: #8d8d8d;
    border-top: 2px solid gray;
    transition: all 0.5s ease;
    position: absolute;
    top: 100%;
    /* left: 117px; */
    width: 100vw;


    .dropdown-container {
      display: flex;
      align-items: center;
      align-content: center;
      width: 100%;
      height: fit-content;
      background-color: #101010;
    }

    h4 {
      margin-bottom: 5px;
      font-size: 18px;
      font-weight: 500;
      line-height: 22.68px;
    }

    p {
      font-size: 16px;
      font-weight: 300;
      line-height: 20.16px;
    }

    &.hidden {
      display: none;
    }

    .container {
      display: flex;
      align-items: center;
      align-content: center;
      justify-content: center;
      width: 100%;
      height: 100%;
      gap: 8%;
      // padding: 0 0 0 180px;
      min-height: 100px;
      font-size: 16px;

      // border: 1px solid green;

      &.Solution {
        height: 360px;
        align-items: baseline;

        .section {
          display: flex;
          flex-direction: column;
          width: 300px;
          // border: 1px solid grey;

          .section-heading.second {
            margin-top: 60px;
          }

          .section-heading {
            display: flex;
            width: 100%;
            // height: 40px;
            align-items: center;
            // color: #fff;
            font-family: "Outfit";
            font-style: normal;
            font-weight: 500;
            font-size: 18px;
            line-height: 23px;
            color: #8d8d8d;
            margin-top: 40px;

            &:hover {
              h4 {
                color: #ffffff;
              }

              p {
                color: #fff;
              }
            }
          }

          .section-content {
            display: flex;
            width: 100%;
            margin-left: -10%;
            padding: 2px 0;

            .icon {
              display: flex;
              width: 10%;
              height: 100%;
              align-items: center;
              justify-content: center;
              // border: 1px solid grey;

              .img {
                display: none;
              }
            }

            .item {
              display: flex;
              width: 90%;
              height: 100%;
              align-items: center;
              // border: 1px solid grey;
              font-family: "Outfit";
              font-style: normal;
              font-weight: 300;
              font-size: 16px;
              line-height: 20px;
              color: #8d8d8d;
              margin-top: 2px;
            }

            &:hover {
              .icon {
                .img {
                  display: block;
                  margin-top: 6px;
                }
              }

              .item {
                color: #008b80;
              }
            }
          }
        }

        .img {
          display: none;
        }

        .img {
          display: block;
          height: 12px;
          // margin-block: -2px;
        }
      }

      .menu-item {
        font-family: "Outfit";
        font-style: normal;
        font-weight: 500;
        font-size: 18px;
        line-height: 23px;
        color: #8d8d8d;

        &:hover {
          color: #fff;
        }
      }
    }
  }

  &.hidden {
    transform: translate3d(0, -100%, 0);
  }

  .logo-container {
    display: flex;
    align-items: center;
    justify-content: center;
    margin-left: -12px;
    margin-top: 12px;
  }

  .menu-container {
    display: flex;
    flex-direction: row;
    align-items: center;
    align-content: center;
    justify-content: center;
    position: relative;
    width: 100%;
    padding-left: 0 !important;
    list-style-type: none;

    .menu-item {
      font-weight: 500;
      font-size: 18px;
      line-height: 20px;
      height: 100%;
      // text-transform: uppercase
      cursor: pointer;
      transition: all 0.3s ease;
      color: #8d8d8d;
      width: 200px;
      position: relative;

      .container {
        display: flex;
        width: 100%;
        height: 100%;
        height: 50px;
        flex-direction: column;
        margin-top: 20px;

        .title {
          display: flex;
          width: 100%;
          height: 60%;
          align-items: center;
          justify-content: center;
          user-select: none;
          font-family: "Outfit" !important;
          padding-bottom: 12px;
        }

        .dropdown-icon {
          display: flex;
          align-items: center;
          justify-content: center;
          width: 100%;
          height: 40%;
        }
      }

      &:hover {
        color: #fff;
      }

      .img {
        display: none;
      }

      &.selected {
        color: #fff;

        .img {
          display: block;
          height: 8px;
          // margin-block: -2px;
        }
      }
    }
  }

  .active-link {
    color: #ffffff !important;
  }
}

@media screen and (max-width: 950px) {
  .header-container {
    display: none;
  }
}
</style>
<script>
import ConnectModal from "../ModalForm/ConnectModal.vue";

export default {
  components: {
    ConnectModal,
  },
  data () {
    return {
      showNavbar: true,
      showDropdown: true,
      toggleTab: null,
      clicked: false,
      showModal: false,
    };
  },

  mounted () {
    window.addEventListener("scroll", this.onScroll);
  },
  beforeDestroy () {
    window.removeEventListener("scroll", this.onScroll);
  },
  methods: {
    onScroll () {
      // Get the current scroll position
      const currentScrollPosition =
        window.pageYOffset || document.documentElement.scrollTop; // Because of momentum scrolling on mobiles, we shouldn't continue if it is less than zero
      if (currentScrollPosition < 0) {
        return;
      } // Here we determine whether we need to show or hide the navbar
      if (currentScrollPosition < this.lastScrollPosition) {
        this.showNavbar = true
      } else {
        this.showNavbar = false
      }
      // this.showNavbar = currentScrollPosition < this.lastScrollPosition; // Set the current scroll position as the last scroll position
      this.lastScrollPosition = currentScrollPosition;
      if (!this.showNavbar) {
        this.showDropdown = false;
      }
    },

    scrollToLocation () {
      if (this.$route.hash) {
        const anchor = document.querySelector(`${this.$route.hash}`);
        if (anchor) {
          window.scrollTo({
            top: anchor.getBoundingClientRect().top + window.pageYOffset,
          });
        }
      }
    },

    onToggleDropdown (tab) {
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
  },
};
</script>
