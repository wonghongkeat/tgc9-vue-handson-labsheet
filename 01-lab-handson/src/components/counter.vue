<template>
  <div>
    <p v-if="number%2==0" v-bind:style='{"color":thiscolor}'>{{ number }}</p>
    <p v-else v-bind:style='{"color":thatcolor}'>{{ number }}</p>

    <button v-on:click="increase">increase</button>
    <button v-on:click="decrease">decrease</button>
     <span v-if="number%2==0" v-bind:style='{"color":thiscolor}'>Even</span>
      <span v-else v-bind:style='{"color":thatcolor}'>Odd</span>
  </div>
</template>



<script>
export default {
  data: function () {
    return {
      number: 0,
      thiscolor: 'green',
      thatcolor: 'red',
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
#green{
    color: green;
}

</style>