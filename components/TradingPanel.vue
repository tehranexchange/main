<template>
<div>
            <v-tabs
          v-model="tradingpaneltabs"
          color="white"
          show-arrows="false"
        >
          <v-tabs-slider color="yellow"></v-tabs-slider>

          <v-tab
            class="px-0"
            active-class="secondary"
          >
            حد ضرر
          </v-tab>
                    <v-tab
            class="px-0"
            active-class="secondary"
          >
            خرید و فروش سریع
          </v-tab>
                    <v-tab
            class="px-0"
            active-class="secondary"
          >
            ثبت سفارش
          </v-tab>
        </v-tabs>
        <v-tabs-items v-model="tradingpaneltabs">
      <v-tab-item>
        <SubmitOffer />
      </v-tab-item>
           <v-tab-item>
        <SubmitOffer />
      </v-tab-item>
           <v-tab-item>
        <SubmitOffer />
      </v-tab-item>
    </v-tabs-items>    
</div>
</template>
<script>
export default {
    name:'TradingPanel',
    data(){
        return{
          tradingpaneltabs:0,
                    items: [
          'ثبت سفارش', 'خرید و فروش سریع', 'حد ضرر',
        ],
        }
    }
}
</script>