<template>
    <VueTradingView :options="{
      symbol: 'NASDAQ:AAPL',
      theme: 'dark',
      locale: 'fa_IR',
        width: '100%',
  height: '98%',
    }" />
</template>
<script>
export default {
    name:'TradingView'
}
</script>