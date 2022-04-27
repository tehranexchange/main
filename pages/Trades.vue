<template>
<!-- <v-row no-gutters>
    <v-col md="3">
        <TradingPanel />
    </v-col>
    <v-col>
<v-row no-gutters>
    <v-col md="4">
        <OfferTables :data='sellers'/>
         <OfferTables :data='buyers' class="my-3" />
                  <OfferTables :data='latest' />
    </v-col>
        <v-col md="8">
<TradingView />
<MyOffers />
</v-col>
</v-row>
    </v-col>
</v-row> -->
    <Resize style="width:100vw; height: 100vh" dir="ltr">
            <DragCol height="100%" width="100%" :leftPercent="80">
        <template #right >
        <TradingPanel dir="rtl" />
        </template>
        <template #left>
         <DragCol height="100%" width="100%" :leftPercent="70">
        <template #right>
          <DragRow height="100%" width="100%" :topPercent="70">
    <template #top>
                    <DragRow height="100%" width="100%">
    <template #top>
                <OfferTables :data='sellers' dir="rtl"/>
    </template>
    <template #bottom>
               <OfferTables :data='buyers' dir="rtl" />
    </template>
  </DragRow> 
    </template>
    <template #bottom>
                  <OfferTables :data='latest' dir="rtl" />
    </template>
  </DragRow>
        </template>
        <template #left>
          <DragRow height="100%" width="100%" :topPercent="65">
    <template #top>
      <TradeDetails dir="rtl"/>
<TradingView dir="rtl" />
    </template>
    <template #bottom>
      <!-- <span class="spark--left"></span> -->
<MyOffers dir="rtl" />
    </template>
  </DragRow>
        </template>
      </DragCol>
        </template>
      </DragCol>
  
</Resize>

</template>
<script>
export default {
    name:'Trades',
    data(){
        return{
            sellers:{
              type:'Sell',
                title: 'فروشندگان',
                min:'400000',
                currency: 'BTC',
                theme: 'red',
                offers:[
                    {
            amount: 0.03,
            unit: 33000000,
            total: 10000000,
          },          
          {
            amount: 0.004,
            unit: 32500000,
            total: 2000000,
          },
                    {
            amount: 1.2,
            unit: 34400000,
            total: 38000000,
          },
                    {
            amount: 0.0003,
            unit: 33300000,
            total: 400000,
          },
                    {
            amount: 2,
            unit: 34000000,
            total: 68000000,
          },
                    {
            amount: 0.05,
            unit: 34000000,
            total: 17000000,
          },
                    {
            amount: 0.6,
            unit: 34000000,
            total: 19000000,
          },
                              {
            amount: 0.68,
            unit: 34000000,
            total: 19600000,
          },
                ]
            },
            buyers:{
              type:'Buy',
                title: 'خریداران',
                min:'68000000',
                currency: 'BTC',
                theme: 'green',
                offers:[
                    {
            amount: 0.03,
            unit: 34000000,
            total: 10000000,
          },          
          {
            amount: 0.004,
            unit: 34000000,
            total: 2000000,
          },
                    {
            amount: 1.2,
            unit: 34000000,
            total: 38000000,
          },
                    {
            amount: 0.0003,
            unit: 34000000,
            total: 400000,
          },
                    {
            amount: 2,
            unit: 34000000,
            total: 68000000,
          },
                    {
            amount: 0.05,
            unit: 34000000,
            total: 17000000,
          },
                    {
            amount: 0.6,
            unit: 34000000,
            total: 19000000,
          },
                              {
            amount: 0.68,
            unit: 34000000,
            total: 19600000,
          },
                ]
            },
             latest:{
                title: 'آخرین معاملات انجام شده',
                min:'68000000',
                currency: 'BTC',
                theme: 'success',
                offers:[
                    {
            amount: 0.03,
            unit: 34000000,
            total: 10000000,
          },          
          {
            amount: 0.004,
            unit: 34000000,
            total: 2000000,
          },
                    {
            amount: 1.2,
            unit: 34000000,
            total: 38000000,
          },
                    {
            amount: 0.0003,
            unit: 34000000,
            total: 400000,
          },
                    {
            amount: 2,
            unit: 34000000,
            total: 68000000,
          },
                    {
            amount: 0.05,
            unit: 34000000,
            total: 17000000,
          },
                    {
            amount: 0.6,
            unit: 34000000,
            total: 19000000,
          },
                              {
            amount: 0.68,
            unit: 34000000,
            total: 19600000,
          },
                ]
            },
        }
    }
}
</script>