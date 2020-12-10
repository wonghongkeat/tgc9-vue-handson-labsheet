<template>
  <div id="app">
    <div>
      <label>Enter your last name</label>
      <input type="text" v-model="lastname" />
      <p>{{firstnameproperty}}</p>
    </div>
  <div>
      <label>Occupation</label>
      <input type='radio' name='job' value='student' v-model='occupation'/>student
      <input type='radio' name='job' value='full-time' v-model='occupation'/>full time
      <input type='radio' name='job' value='part-time' v-model='occupation'/>part time
  </div>
  <div>
      <label>free time</label>
      <input type='checkbox' name='free' value='sports' v-model='leisure'/>sports
      <input type='checkbox' name='free' value='reading' v-model='leisure'/>reading
      <input type='checkbox' name='free' value='sleeping' v-model='leisure'/>sleeping
      <input type='checkbox' name='free' value='eating' v-model='leisure'/>eating
      <input type='checkbox' name='free' value='hanging' v-model='leisure'/>hanging
  </div>
  <div>
            <label>where are you from</label>
            <select v-model='country'>
                <option value="singapore">Singapore</option>
                <option value="malaysia">malaysia</option>
                <option value="thailand">thailand</option>
            </select>
        </div>
    <h2>your details</h2>
    <h3>{{ lastname }}</h3>
    <h3>{{occupation}}</h3>
    <h3>{{leisure}}</h3>
    <h3>where are you from: {{country}}</h3>

  <div>
      <label>Please enter two numbers</label>
      <input type='text' v-model='number1'>
      <input type='text' v-model='number2'>
      <button v-on:click='addition'>add</button>
  </div>
    <h3>the total sum is: {{number3}}</h3>
    <h3>the auto sum is: {{results}}</h3>

  </div>
</template>

<script>
export default {
  data: function () {
    return {
      lastname: "",
      occupation:'',
      leisure: [],
      country:'',
      number1:'',
      number2:'',
      number3:''
    };
  },
  methods: {
      addition: function(){
          this.number3 = parseInt(this.number1) + parseInt(this.number2)
      }
  },
  computed:{
      results:function(){
          return parseInt(this.number1) + parseInt(this.number2)
      } ,
    //   'firstnameproperty': function(){
    //       if (this.lastname.length < 3){
    //             return "please enter more than 3 characters"
    //       }else{
    //           return this.warning = ''
    //       }
    //   }
}
}
</script>

<style>
h3{
    border: 2px black solid;
    height: 30px;
    width: 50vw;
    color: red;
}
</style>
