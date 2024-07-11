<template>
  <h3>History</h3>
  <ul id="list" class="list">
    <!-- <li class="minus">
      Cash <span>-$400</span><button class="delete-btn">x</button>
    </li>
    <li class="plus">
      PayCheck <span>$800</span><button class="delete-btn">x</button>
    </li> -->
    <li
      v-for="transaction in transactions"
      :key="transaction.id"
      :class="transaction.amount < 0 ? 'minus' : 'plus'"
    >
      {{ transaction.text }} <span>{{ transaction.amount }}</span
      ><button class="delete-btn">x</button>
    </li>
  </ul>
</template>
<script>
export default {
  data() {
    return {
      transactions: [
        { id: 1, text: "Flower", amount: -19.99 },
        { id: 2, text: "Salary", amount: 299.0 },
        { id: 3, text: "Book", amount: -10.0 },
      ],
    };
  },
};
</script>
