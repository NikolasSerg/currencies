<template>
  <div class="container">
    <table class="table table-secondary table-striped">
      <thead>
        <tr>
          <th class="fs-4">Знак валюты</th>
          <th class="fs-4">Название валюты</th>
          <th class="fs-4">Курс</th>
        </tr>
      </thead>
      <tbody>
        <CurrenciesItem
          v-for="coin of curr"
          v-bind:coin="coin"
          v-bind:key="coin.Cur_ID"
          
        />
      </tbody>
    </table>
  </div>
</template>
<script>
import CurrenciesItem from "@/components/currenciesItem";
export default {
  props: ["curr"],
  name: "CurrenciesList",
  components: {
    CurrenciesItem,
  },
};
</script>
<style></style>
