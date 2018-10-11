<template>
  <div>
    <app-stock v-for="stock in stocks" :key="stock.id"></app-stock>
  </div>
</template>

<script>
import Stock from './Stock.vue';
export default {
  name: 'Stocks',
  data() {
    return {
      stocks: [
        { id: 1, name: 'BMW', price: 110},
        { id: 2, name: 'APPL', price: 123},
        { id: 3, name: 'TSLA', price: 143},
        { id: 4, name: 'AMZN', price: 1939}
      ]
    }
  },
  components: {
    appStock: Stock
  }
}
</script>