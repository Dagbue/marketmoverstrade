<template>
  <div class="tradingview-widget-container">
    <div ref="widgetContainer" class="tradingview-widget-container__widget"></div>
    <div class="tradingview-widget-copyright">
      <a href="https://www.tradingview.com/" rel="noopener nofollow" target="_blank">
        <span class="blue-text"></span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "UsdcWidget",
  mounted() {
    if (typeof TradingView === 'undefined') {
      const script = document.createElement('script');
      script.src = 'https://s3.tradingview.com/external-embedding/embed-widget-mini-symbol-overview.js';
      script.async = true;
      script.innerHTML = JSON.stringify({
        "symbol": "COINBASE:SOLUSD",
        "width": 300,
        "height": 320,
        "locale": "en",
        "dateRange": "12M",
        "colorTheme": "dark",
        "isTransparent": false,
        "autosize": false,
        "largeChartUrl": ""
      });
      this.$refs.widgetContainer.appendChild(script);
    }
  }
}
</script>

<style scoped>

</style>