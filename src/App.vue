<template>
  <div id="app">
    <CurrenciesList 
      v-bind:curr = "currencies"
    />
  </div>
</template>

<script>
import CurrenciesList from "@/components/currenciesList";
export default {
  name: "App",
  data() {
    return {
      currencies: [

      ]
    }
  },
  mounted() {
    fetch("https://www.nbrb.by/api/exrates/rates?periodicity=0")
    .then(response => response.json())
    .then(data => {
      this.currencies = data
    })
  },
  components: {
    CurrenciesList
  },
};
</script>

<style>

</style>
