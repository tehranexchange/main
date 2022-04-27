<template>
<v-card tile flat>
      <v-card-title class="pa-2">
        {{this.data.title}}
        <span class="mr-auto"
        v-text="this.data.type === 'Sell' ? this.min : this.max"
         :class="data.type === 'Sell' ? 'red--text' : 'success--text'"></span>
      </v-card-title>
   <v-data-table
   class="accent rounded-0"
    :headers="headers"
    :items="this.data.offers"
    :items-per-page="8"
    hide-default-footer
    dense
    :style="tr"
  >
   <template v-slot:item="{ item }">
  <tr>
    <td>{{ item.amount }}</td>
    <td>{{ item.unit }}</td>
    <td :class="data.type === 'Sell' ? 'red--text' : 'success--text'">{{ item.total }}</td>
  </tr>
</template>
  </v-data-table>   
</v-card>
</template>
<script>
export default {
    name:'OfferTables',
    props:['data'],
    data(){
        return{
          units:[],
          max:null,
          min:null,
          headers: [
          {
            text: `مقدار (${this.data.currency})`,
            align: 'start',
            sortable: false,
            value: 'amount',
          },
          { text: 'قیمت واحد (تومان)', value: 'unit', sortable: true,},
          { text: 'قیمت کل(تومان)', value: 'total', sortable: false, },
        ],
        }
    },
    methods:{
      getMinMax(){
            for(let i =0; i<this.data.offers.length; i++){
              this.units.push(this.data.offers[i].unit)
    }
     this.max = Math.max(...this.units)
     this.min = Math.min(...this.units)
      }
    },
  computed: {
    tr() {
      return {
        "background": `linear-gradient(to left, ${this.data.theme} ${this.ratio}, transparent ${this.ratioReverse})`
}
    }
  },
  mounted(){
    this.getMinMax()
  }
}
</script>
<style>
.style-1{
}
.style-2{
background-color: red !important;
}
</style>