<template>
  <Header />
  <div class="container">
    <Balance />
    <IncomeExpenses />
    <TransactionList :transactions="transactions" />
    <AddTransaction />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Balance from './components/Balance.vue';
import IncomeExpenses from './components/IncomeExpenses.vue';
import TransactionList from './components/TransactionList.vue';
import AddTransaction from './components/AddTransaction.vue';

export default {
  components: {
    Header,
    Balance,
    IncomeExpenses,
    TransactionList,
    AddTransaction,
  },
};

import { defineProps } from 'vue';

const props = defineProps({
  transactions: {
    type: Array,
    required: true,
  },
});
</script>
