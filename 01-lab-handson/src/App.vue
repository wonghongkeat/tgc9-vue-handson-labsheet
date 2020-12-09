<template>
  <div id="app">
    <Greeting />
    <Counter/>
    <Dice/>
  </div>
</template>

<script>

import Greeting from './components/sayGreetings';
import Counter from './components/counter'
import Dice from './components/dice'

export default {
  name: '#app',
  components: {
      Greeting, Counter,Dice
  
}
}
</script>

<style>
</style>
