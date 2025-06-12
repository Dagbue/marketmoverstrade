<template>
  <div class="tradingview-widget-container">
    <div class="tradingview-widget-container__widget" ref="widget"></div>
    <div class="tradingview-widget-copyright">
      <a
          href="https://www.tradingview.com/"
          rel="noopener nofollow"
          target="_blank"
      >
        <span class="blue-text"></span>
      </a>
    </div>
  </div>
</template>


<script>
export default {
  name: "ChfWidget",
  mounted() {
    // Create the script element
    const script = document.createElement('script');
    script.type = 'text/javascript';
    script.src = 'https://s3.tradingview.com/external-embedding/embed-widget-mini-symbol-overview.js';
    script.async = true;
    script.innerHTML = JSON.stringify({
      symbol: 'OANDA:CHFJPY',
      width: 300,
      height: 320,
      locale: 'en',
      dateRange: '12M',
      colorTheme: 'dark',
      isTransparent: false,
      autosize: false,
      largeChartUrl: '',
    });

    // Append script to the widget container
    this.$refs.widget.appendChild(script);
  },
}
</script>

<style scoped>
.tradingview-widget-container {

}
</style>