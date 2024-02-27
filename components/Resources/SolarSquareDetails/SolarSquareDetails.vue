<template>
   <div class="details-container">
      <div class="challenges-wrapper">
         <label class="challenges">Challenges</label>
         <ul>
            <li>Non standardized BOQ impacts ROI negatively.(high inventory carrying cost and operational expenses)</li>
            <li>Non-Scalable warehouses, requiring frequent relocation</li>
            <li>High ratio of product damage, delay in installation with high logistics cost.</li>
            <li>Require specialized handling for fragile and costly parts.</li>
         </ul>
      </div>
      <div class="solution-wrapper">
         <label class="solution">Solution</label>
         <ul>
            <li>Network design for regional warehouse and fulfillment centre starting from site selection, WH finalization,
               Infra installation and commissioning and Go live.</li>
            <li>Standardized kits dispatch from regional warehouse for easy tracking and installations</li>
            <li>Designing of Multimodal transport system for Hub and spoke Fulfillment model with standardized stuffing for
               FTL and PTL movements.</li>
         </ul>
      </div>
      <div class="result-wrapper">
         <label class="result">Results</label>
         <ul>
            <li>Reduction of 35% in warehousing and manpower handling cost.</li>
            <li>ROI increase by 25% warehouses for covering.</li>
            <li>69% of tier 2 cities being served on SDD model.</li>
         </ul>
      </div>
      <div class="key-numbers-wrapper">
         <label class="keynumbers">Key numbers</label>
         <ul>
            <li>No. of current warehouse - 10</li>
            <li>Warehouses Planned- 15</li>
            <li>Total Space - 60000 sq ft</li>
         </ul>
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
   .solution-wrapper,
   .key-numbers-wrapper {
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
   }
}

@media screen and (max-width: 850px) {
   .details-container {

      .challenges-wrapper,
      .result-wrapper,
      .solution-wrapper,
      .key-numbers-wrapper {
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
      }
   }
}
</style>