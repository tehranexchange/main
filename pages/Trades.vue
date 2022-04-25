<template>
<v-row no-gutters>
    <v-col md="3">
        <TradingPanel />
    </v-col>
    <v-col>
<v-row no-gutters>
    <v-col md="4">
        <OfferTables />
         <OfferTables />
    </v-col>
        <v-col md="8">
<TradingView />
</v-col>
</v-row>
    </v-col>
</v-row>

</template>
<script>
import TradingPanel from '../components/TradingPanel.vue'
export default {
  components: { TradingPanel },
    name:'Trades',
}
</script>