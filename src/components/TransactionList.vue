<template>
  <h3>History</h3>
  <ul id="list" class="list">
    <li v-for="transaction in transactions" :key="transaction.id">
      {{ transaction.text }} <span>-${{ transaction.amount }}</span
      ><button class="delete-btn">x</button>
    </li>

    <li class="plus">
      Paycheck <span>$800</span><button class="delete-btn">X</button>
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      transactions: [{ id: 1, text: 'Flower', amount: -19.99 }],
    };
  },
};
</script>
