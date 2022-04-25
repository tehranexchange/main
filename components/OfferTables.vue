<template>
<v-card tile flat>
   <v-data-table
    :headers="headers"
    :items="offers"
    :items-per-page="5"
    hide-default-footer
    dense
  ></v-data-table>   
</v-card>
</template>
<script>
export default {
    name:'OfferTables',
    data(){
        return{
          currency:'BTC',
                    headers: [
          {
            text: `مقدار(${`btc`})`,
            align: 'start',
            sortable: false,
            value: 'amount',
          },
          { text: 'قیمت واحد (تومان)', value: 'unit' },
          { text: 'قیمت کل(تومان)', value: 'total' },
        ],
        offers: [
          {
            amount: 1,
            unit: 1,
            total: 1,
          },          
          {
            amount: 1,
            unit: 1,
            total: 1,
          },
                    {
            amount: 1,
            unit: 1,
            total: 1,
          },
                    {
            amount: 1,
            unit: 1,
            total: 1,
          },
                    {
            amount: 1,
            unit: 1,
            total: 1,
          },
                    {
            amount: 1,
            unit: 1,
            total: 1,
          },
                    {
            amount: 1,
            unit: 1,
            total: 1,
          },
        ],
        }
    }
}
</script>