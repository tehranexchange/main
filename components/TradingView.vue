<template>
    <VueTradingView :options="{
      symbol: 'NASDAQ:AAPL',
      theme: 'dark',
      locale: 'fa_IR',
        width: '100%',
  height: '500px',
    }" />
</template>
<script>
export default {
    name:'TradingView'
}
</script>