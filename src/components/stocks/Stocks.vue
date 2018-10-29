<template>
  <div>
    <h1>Stocks View</h1>
    <st-stock v-bind:key="index" v-for="(stock, index) in stocks" :stock="stock"></st-stock>
  </div>
</template>

<script>
import Stock from "./Stock.vue";

export default {
  components: {
    "st-stock": Stock
  },
  computed: {
    stocks() {
      return this.$store.getters.stocks;
    }
  }
};
</script>