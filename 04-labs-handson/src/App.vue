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
  <br>
  <hr>
  <br>
  <Services/>
  </div>
</template>

<script>

import Form from './components/form';
import Sign from './components/SignupForm';
import Validation from './components/validation';
import Services from './components/services'

export default {
  name: '#app',
  components: {
      Form, Sign, Validation,Services
  
}
}
</script>

<style>

</style>
