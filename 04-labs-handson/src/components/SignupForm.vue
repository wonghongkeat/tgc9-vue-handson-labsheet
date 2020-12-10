<template>
    <div>
        <h1>Please enter your details</h1>
    <div>
<label>Name</label>
<input type='text' v-model='name'/>
    </div>
    <div>
        <label>Prgramming background</label>
        <input type='radio' name='background' value='no-experience' v-model='background'/>no experience
        <input type='radio' name='background' value='intermediate' v-model='background'/>intermediate
        <input type='radio' name='background' value='eperienced' v-model='background'/>experienced
    </div>
    <div>
        <label>interested programming language</label>
        <input type='checkbox' name='language' value='Java' v-model='language'/>Java
         <input type='checkbox' name='language' value='Python' v-model='language'/>Python
          <input type='checkbox' name='language' value='C++' v-model='language'/>C++
           <input type='checkbox' name='language' value='JavaScript' v-model='language'/>JavaScript
    </div>
    <div>
        <label>preferred timing</label>
        <select v-model='timing'>
            <option value='morning'>morning</option>
            <option value='afternoon'>afternoon</option>
            <option value='evening'>evening</option>
        </select>
    </div>

    </div>
</template>

<script>
export default {
    data: function(){
        return{
            name:'',
            background:'',
            language:[],
            timing:''
        }
    }
}
</script>

<style scoped>

</style>