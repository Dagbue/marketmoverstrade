<template>
  <div class="tradingview-widget-container">
    <div ref="tvWidget" class="tradingview-widget-container__widget"></div>
    <div class="tradingview-widget-copyright">
      <a href="https://www.tradingview.com/" rel="noopener nofollow" target="_blank">
        <span class="blue-text"></span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "EthWidget",
  mounted() {
    const script = document.createElement("script");
    script.type = "text/javascript";
    script.src = "https://s3.tradingview.com/external-embedding/embed-widget-mini-symbol-overview.js";
    script.async = true;
    script.innerHTML = JSON.stringify({
      symbol: "BINANCE:ETHUSDT",
      width: 300,
      height: 320,
      locale: "en",
      dateRange: "12M",
      colorTheme: "dark",
      isTransparent: false,
      autosize: false,
      largeChartUrl: ""
    });
    this.$refs.tvWidget.appendChild(script);
  }
}
</script>

<style scoped>

</style>