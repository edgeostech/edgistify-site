<template>
   <div class="case-studies-container">
      <div class="case-studies-wrapper" id="resource-Case-studies">
         <div class="top-header">
            <h1 class="page-title">Case Studies</h1>

            <div class="buttons-container">
               <v-btn icon @click="scrollLeft">
                  <v-icon>
                     mdi-arrow-left-circle-outline
                  </v-icon>
               </v-btn>
               <v-btn icon @click="scrollRight"><v-icon>
                     mdi-arrow-right-circle-outline
                  </v-icon></v-btn>
            </div>
         </div>
         <div class="case-studies-wrapper-row" id="case-studies-content">
            <div class="specialists-details" v-if="$route.name.split('-')[1] !== 'bisleri'">
               <label>Bisleri</label>
               <v-img src="/Resource/study3.png" class="img"></v-img>
               <div class="info-text">
                  <h1>
                     Bisleri International is an Indian company that is best known for its eponymous brand of bottled water
                  </h1>
                  <nuxt-link to="/resources/bisleri" style="text-decoration: none; color: inherit">
                     <p>Read More</p>
                  </nuxt-link>
               </div>
            </div>
            <div class="specialists-details" v-if="$route.name.split('-')[1] !== 'solarSquare'">
               <label>Solar Square</label>
               <v-img src="/Resource/study2.png" class="img"></v-img>
               <div class="info-text">
                  <h1>
                     Solar Square is one of the leading residential rooftop solar installation companies. It has penetrated
                     not only in metros but also in tier 1 and tier 2 cities of India
                  </h1>
                  <nuxt-link to="/resources/solarSquare" style="text-decoration: none; color: inherit">
                     <p>Read More</p>
                  </nuxt-link>
               </div>
            </div>
            <div class="specialists-details" v-if="$route.name.split('-')[1] !== 'saveo'">
               <label>Saveo</label>
               <v-img src="/Resource/study4.png" class="img"></v-img>
               <div class="info-text">
                  <h1>
                     Saveo is a B2B brand that buys medicines from wholesalers and delivers to retailers (Marketplace of
                     medicine). They are majorly present in AP, Telangana and Karnata...
                  </h1>
                  <nuxt-link to="/resources/saveo" style="text-decoration: none; color: inherit">
                     <p>Read More</p>
                  </nuxt-link>
               </div>
            </div>
            <div class="specialists-details" v-if="$route.name.split('-')[1] !== 'apnaMart'">
               <label>Apna Mart</label>
               <v-img src="/Resource/study1.png" class="img"></v-img>
               <div class="info-text">
                  <h1>
                     Apna Mart operates a multi-level retail distribution network with 100+ stores in Chhattisgarh &
                     Jharkhand
                  </h1>
                  <nuxt-link to="/resources/apnaMart" style="text-decoration: none; color: inherit">
                     <p>Read More</p>
                  </nuxt-link>
               </div>
            </div>
         </div>

      </div>
   </div>
</template>
<script>


export default {
   data () {
      return {
         scrollAmount: 0
      }
   },
   methods: {
      scrollLeft () {
         document.querySelector('.case-studies-wrapper-row').scrollBy(-200, 0)
      },
      scrollRight () {
         document.querySelector('.case-studies-wrapper-row').scrollBy(200, 0)
      },
   }
}

</script>
 
<style lang="scss" scoped>


.case-studies-container {
   width: 100%;
   height: auto;
   background: #f3f3f5;

   .case-studies-wrapper {
      width: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;

      .top-header {
         display: flex;
         align-items: center;
         justify-content: space-between;
         padding-right: 3%;

         h1.page-title {
            font-family: "Noto Serif";
            font-style: normal;
            font-weight: 300;
            font-size: 42px;
            line-height: 63px;
            color: #0c0c0c;
            margin: 2% 0 2% 7%;
         }

      }



      .case-studies-wrapper-row {
         width: 100%;
         display: flex;
         justify-content: space-evenly;
         margin-bottom: 2rem;
         overflow-x: scroll;
         scroll-behavior: smooth;
         height: 620px;
         padding-left: 42%;

         label {
            font-family: 'Noto Serif';
            font-style: normal;
            font-weight: 400;
            font-size: 24px;
            line-height: 33px;
            color: #1E1E1E;
            display: block;
            margin-bottom: 24px;
         }

         .specialists-details:hover {
            .img {
               filter: grayscale(0%);
               transition: all 1s ease-in-out;

            }

            .info-text p {
               color: #00a699;
            }
         }

         .specialists-details {
            width: 603px;
            height: 404px;
            margin: 2rem;

            .img {
               width: 603px;
               height: 404px;
               margin-bottom: 1rem;
               filter: grayscale(100%)
            }


            .info-text {
               width: 100%;

               h1 {
                  font-family: 'Outfit';
                  font-style: normal;
                  font-weight: 300;
                  font-size: 16px;
                  line-height: 20px;
                  color: #313131;
                  margin-bottom: 1rem;
               }

               p {
                  font-family: 'Noto Serif';
                  font-style: normal;
                  font-weight: 400;
                  font-size: 16px;
                  line-height: 22px;
                  color: #616161;
               }
            }
         }
      }

      .case-studies-wrapper-row::-webkit-scrollbar {
         display: none;
      }

      .case-studies-wrapper-row {
         -ms-overflow-style: none;
         scrollbar-width: none;
      }
   }
}

@media (max-width: 850px) {

.top-header {

      h1.page-title {
         font-size: 32px !important;
      }
   }
.case-studies-container {
   height: auto !important;

   .case-studies-wrapper {
      align-items: flex-start !important;
      width: 100% !important;

      .top-header {
         display: flex;
         align-items: center;
         justify-content: space-between;
         padding-right: 5% !important;
         width: 100% !important;

         h1 {
            font-family: 'Noto Serif' !important;
            font-style: normal !important;
            font-weight: 300 !important;
            font-size: 24px !important;
            line-height: 33px !important;
            color: #0C0C0C !important;
            margin: 2% 0 2% 7%;
         }
      }


   }

   .case-studies-wrapper-row {
      justify-content: flex-start !important;
      margin-bottom: 0 !important;
      height: auto !important;
      flex-direction: row !important;
      padding-left: 2% !important;

      label {
         font-size: 12.4071px !important;
         line-height: 17px !important;
      }


      .specialists-details {
         height: auto !important;
         width: 90% !important;
         height: auto !important;
         margin: 0rem !important;
         margin: 20px 0 20px 20px !important;

         .img {
            width: 90% !important;
            height: 45% !important;
         }

         .info-text {
            width: 88% !important;
            white-space: pre-line !important;
            font-size: 12px !important;

            h1 {
               font-size: 8.27141px !important;
               line-height: 10px !important;
               margin-bottom: 1rem !important;
            }

            p {
               font-size: 8.27141px !important;
               line-height: 11px !important;

            }

         }
      }
   }
}
}
</style>
 