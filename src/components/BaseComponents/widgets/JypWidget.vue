<template>
  <div class="tradingview-widget-container">
    <div class="tradingview-widget-container__widget" ref="widgetContainer"></div>
    <div class="tradingview-widget-copyright">
      <a href="https://www.tradingview.com/" rel="noopener nofollow" target="_blank">
        <span class="blue-text"></span>
      </a>
    </div>
  </div>
</template>


<script>
export default {
  name: "JypWidget",
  mounted() {
    // Check if the script already exists
    if (document.getElementById("tradingview-widget-script")) {
      this.createWidget();
    } else {
      const script = document.createElement("script");
      script.id = "tradingview-widget-script";
      script.src = "https://s3.tradingview.com/external-embedding/embed-widget-mini-symbol-overview.js";
      script.async = true;
      script.innerHTML = JSON.stringify({
        symbol: "OANDA:EURJPY",
        width: 300,
        height: 320,
        locale: "en",
        dateRange: "12M",
        colorTheme: "dark",
        isTransparent: false,
        autosize: false,
        largeChartUrl: ""
      });
      this.$refs.widgetContainer.appendChild(script);
    }
  },
  methods: {
    createWidget() {
      const container = this.$refs.widgetContainer;
      container.innerHTML = ""; // Clear any existing widget
      const script = document.createElement("script");
      script.src = "https://s3.tradingview.com/external-embedding/embed-widget-mini-symbol-overview.js";
      script.async = true;
      script.innerHTML = JSON.stringify({
        symbol: "OANDA:EURJPY",
        width: 350,
        height: 220,
        locale: "en",
        dateRange: "12M",
        colorTheme: "dark",
        isTransparent: false,
        autosize: false,
        largeChartUrl: ""
      });
      container.appendChild(script);
    }
  }
}
</script>

<style scoped>
.tradingview-widget-container {
}
</style>