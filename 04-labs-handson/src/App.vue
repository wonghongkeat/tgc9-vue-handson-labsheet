<template>
  <div id="app">
  <Form/>
  <br>
  <hr>
  <br>
  <Sign/>
  <br>
  <hr>
  <br>
  <Validation/>
  </div>
</template>

<script>

import Form from './components/form';
import Sign from './components/SignupForm';
import Validation from './components/validation';

export default {
  name: '#app',
  components: {
      Form, Sign, Validation
  
}
}
</script>

<style>

</style>
