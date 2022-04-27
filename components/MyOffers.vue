<template>
    <div>
                    <v-tabs
          v-model="tab"
          color="yellow"
        >
          <v-tabs-slider color="yellow"></v-tabs-slider>
          <v-tab>
              سفارشات فعال من
          </v-tab>
          <v-tab>
              تاریخچه سفارشات
          </v-tab>
        </v-tabs>
        <v-tabs-items v-model="tab">
      <v-tab-item>
        <ActiveOffers />
      </v-tab-item>
       <v-tab-item>
        <OffersHistory />
      </v-tab-item>
    </v-tabs-items>   
    </div>
</template>
<script>
export default {
    name:'MyOffers',
    data(){
        return{
            tab:0
        }
    }
}
</script>
<style >
.v-tabs-slider-wrapper{
  bottom: unset !important;;
  top:0 !important;
}
</style>