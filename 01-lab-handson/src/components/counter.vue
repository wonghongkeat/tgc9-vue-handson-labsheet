<template>
  <div>
    <p>{{ number }}</p>
    <button v-on:click="increase">increase</button>
    <button v-on:click="decrease">decrease</button>
     <span v-if="number%2==0">Even</span>
      <span v-else>Odd</span>
  </div>
</template>



<script>
export default {
  data: function () {
    return {
      number: 0,
    };
  },

  methods: {
    increase: function () {
      this.number += 1;
    },
    decrease: function () {
      this.number -= 1;
    },


  },
};
</script>



<style scoped>
</style>