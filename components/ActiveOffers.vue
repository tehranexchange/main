<template>
     <v-data-table
   class="accent rounded-0"
    :headers="headers"
    :items="this.data"
    :items-per-page="4"
    hide-default-footer
    dense
    :no-data-text="nodata"
  >
  </v-data-table>   
</template>
<script>
export default {
    name:'ActiveOffers',
    props:['data'],
    data(){
        return{
            nodata:'سفارشی یافت نشد',
                      headers: [
          {
            text: `ردیف`,
            align: 'start',
            sortable: true,
            value: 'amount',
          },
          { text: 'نوع', value: 'unit', sortable: false,},
          { text: 'بازار', value: 'total', sortable: false, },
          { text: 'مقدار', value: 'total', sortable: false, },
          { text: 'قیمت واحد', value: 'total', sortable: false, },
        { text: 'قیمت کل', value: 'total', sortable: false, },
        { text: 'پر شده', value: 'total', sortable: false, },
        { text: 'تاريخ ثبت', value: 'total', sortable: false, },
        { text: 'عملیات', value: 'total', sortable: false, },



        ]
        }
    }
}
</script>