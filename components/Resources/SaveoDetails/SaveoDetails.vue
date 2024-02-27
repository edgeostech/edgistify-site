<template>
   <div class="details-container">
      <div class="challenges-wrapper">
         <label class="challenges">Challenges and Requirement</label>
         <ul>
            <li>They make their medicines reach tier 3 cities, towns and villages for which they use passenger bus as mode of
               transportation (cost effective).</li>
            <li>They have warehouses in multiple locations disrupting order synchronization. Their deliveries lacked proper
               management and system.</li>
            <li>On time delivery to tier 1, tier, tier 3 cities, towns and villages following a systematic controllable
               process.</li>
         </ul>
      </div>
      <div class="solution-wrapper">
         <label class="solution">Solution</label>
         <p>We helped them set up a centralized warehouse and streamlined the flow of products. We continued the same mode
            of transportation but with a defined and monitorable process
            ensuring timely delivery followed by cash collection. We defined KRAs and KPI of the manpower involved making it
            easier to track and giving more control of the supply chain to the
            client.</p>
      </div>
      <div class="result-wrapper">
         <label class="result">Results</label>
         <p>With us coming in the client was not only assured of a timely delivery but also had a roadmap of where the
            medicine is exactly because of the structure put in place by Edgistify.
            Additionally we have enabled other modes of payment for Saveo. In a single town they had an outstanding of 70L.
            We successfully managed the cash flow with utmost
            transparency.<br />
            <br />
            We promised 24 hour delivery within the radius of 500 km along with COD. This is a huge commitment as standard
            courier delivery ETA is 48 hours. This was a very customized
            solution in medical business making it reach villages.
         </p>
      </div>
   </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.details-container {
   display: flex;
   width: 100%;
   flex-direction: column;
   height: auto;
   background-color: #ffffff;
   padding: 6.5% 0 0 10%;

   .challenges-wrapper,
   .result-wrapper,
   .solution-wrapper {
      width: 100%;
      height: auto;
      display: flex;
      flex-direction: column;
      padding-bottom: 5%;

      label {
         width: 100%;
         height: auto;
         padding-bottom: 1.5%;
         font-family: 'Noto Serif';
         font-style: normal;
         font-weight: 300;
         font-size: 2.25rem;
         line-height: 3.063rem;
         color: #0C0C0C;
      }

      ul {
         padding-left: 1%;

         li {
            list-style: none;
            font-family: 'Outfit';
            font-style: normal;
            font-weight: 300;
            font-size: 1rem;
            line-height: 1.25rem;
            color: #313131;
         }

         li:before {
            content: "· ";
            font-size: 30px;
            vertical-align: middle;
            line-height: 24px;
         }
      }

      p {
         width: 95%;
         font-family: 'Outfit';
         font-style: normal;
         font-weight: 300;
         font-size: 1rem;
         line-height: 1.25rem;
         color: #313131;
      }
   }
}

@media screen and (max-width: 850px) {
   .details-container {

      .challenges-wrapper,
      .result-wrapper,
      .solution-wrapper {
         padding-bottom: 20% !important;

         label {
            font-size: 1.5rem !important;
            line-height: 2.063rem !important;
         }

         ul {
            padding-left: 1%;
            padding-right: 12% !important;

            li {
               font-size: 0.75rem !important;
               line-height: 0.938rem !important;
            }

            li:before {
               content: "· ";
               font-size: 24px !important;
               line-height: 0px !important;
            }
         }

         p {
            width: 100% !important;
            padding-right: 10% !important;
            font-size: 0.75rem !important;
            line-height: 0.938rem !important;
         }
      }
   }
}
</style>