<template>
   <div class="resources-apnamart-container">
      <div class="head-cover">
         <div class="left-head-cover">
            <div class="title">
               <div class="title_header">
                  <p>
                     Apna Mart operates a multi -level retail distribution network with 100+ stores in Chhattisgarh &
                     Jharkhand
                  </p>
               </div>
            </div>
         </div>
         <div class="right-head-cover">
            <div class="head_image">
               <v-img src="/Resource/extra/apnamart-banner.png" class="apnamart-banner"> </v-img>
            </div>
         </div>
      </div>
      <ApnaMartDetails />
      <CaseStudies />
      <EdgistifyForm />
   </div>
</template>

<script>
import ApnaMartDetails from '../../components/Resources/ApnaMartDetails/ApnaMartDetails.vue';
import CaseStudies from '../../components/Resources/CaseStudies/CaseStudies.vue'
import EdgistifyForm from '../../components/EdgistifyForm/EdgistifyForm.vue'

export default {
   components: {
      ApnaMartDetails,
      CaseStudies,
      EdgistifyForm
   }
}
</script>

<style lang="scss" scoped>
@media (max-width: 850px) {
   .resources-apnamart-container {
      display: flex;
      flex-direction: column;
      width: 100%;
      height: auto;
      background-color: #0c0c0c;

      .head-cover {
         display: flex;
         width: 100%;
         height: auto !important;
         flex-direction: column !important;
         align-items: center;
         justify-content: auto;

         .left-head-cover {
            display: flex;
            width: 100% !important;
            height: auto !important;
            background-position: center;
            background-size: contain;
            justify-content: center;
            background-color: #ffffff;

            .title {
               display: flex;
               width: 100%;
               height: 100%;
               flex-direction: column;
               justify-content: center;
               color: #1e1e1e;

               .title_header {
                  display: flex;
                  padding: 10% 0 0 15% !important;
                  width: 70% !important;
                  height: 100%;

                  p {
                     font-family: 'Noto Serif' !important;
                     font-style: normal !important;
                     font-weight: 300 !important;
                     font-size: 26px !important;
                     line-height: 35px !important;
                     color: #0C0C0C !important;
                  }
               }
            }
         }

         .right-head-cover {
            display: flex;
            width: 100% !important;
            height: auto !important;
            background-color: #ffffff;
            padding: 3rem !important;

            .head_image {
               display: flex;
               width: 100%;
               height: 100%;

               .apnamart-banner {
                  width: 19.063rem !important;
                  height: 13.813rem !important;
               }
            }
         }
      }
   }
}

.resources-apnamart-container {
   display: flex;
   flex-direction: column;
   width: 100%;
   height: auto;
   background-color: #0c0c0c;

   .head-cover {
      display: flex;
      width: 100%;
      height: 555px;
      align-items: center;
      justify-content: auto;

      .left-head-cover {
         display: flex;
         width: 50%;
         height: 555px;
         background-position: center;
         background-size: contain;
         justify-content: center;
         background-color: #ffffff;

         .title {
            display: flex;
            width: 100%;
            height: 100%;
            flex-direction: column;
            justify-content: center;
            color: #1e1e1e;

            .title_header {
               display: flex;
               padding: 85px 0 0 120px;
               width: 85%;
               height: 100%;

               p {
                  font-size: 46.61px;
                  font-weight: 300;
                  font-family: "Noto Serif";
                  font-style: normal;
                  line-height: 63px;
               }
            }
         }
      }

      .right-head-cover {
         display: flex;
         width: 50%;
         height: 555px;
         background-color: #ffffff;
         padding: 5rem;

         .head_image {
            display: flex;
            width: 100%;
            height: 100%;
         }
      }
   }
}
</style>