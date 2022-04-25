<template>
<v-card tile flat>
            <v-tabs
          v-model="tab"
        >
          <v-tabs-slider color="yellow"></v-tabs-slider>

          <v-tab
            v-for="item in items"
            :key="item"
          >
            {{ item }}
          </v-tab>
        </v-tabs>
        <v-tabs-items v-model="tab">
      <v-tab-item
        v-for="item in items"
        :key="item"
      >
        <div>
          <p> blah blah</p>
        </div>
      </v-tab-item>
    </v-tabs-items>    
</v-card>
</template>
<script>
export default {
    name:'TradingPanel',
    data(){
        return{
                    items: [
          'ثبت سفارش', 'خرید و فروش سریع', 'حد ضرر',
        ],
        }
    }
}
</script>