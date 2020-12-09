<template>
  <div id="app">
    <Greeting />
    <Counter />
  </div>
</template>

<script>

import Greeting from './components/sayGreetings';
import Counter from './components/counter'

export default {
  name: '#app',
  components: {
      Greeting, Counter
  
}
}
</script>

<style>
</style>
