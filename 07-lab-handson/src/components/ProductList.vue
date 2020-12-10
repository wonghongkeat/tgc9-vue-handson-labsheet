<template>
  <div>
      <div>
      <h2>Product List</h2>
      <ul>
          <li v-for='(i, index) in product' v-bind:key='index'>
              {{i}}
              <button>X</button>
              <button>edit</button>
            </li>
        </ul>
        </div>
  <div>
      <label>Enter new product:</label>
      <input type='text' v-model='newProduct'>
  </div>
  </div>
</template>

<script>


export default {
data: function(){
    return{
        product: ["Handbags", "Vacuum Cleaner","broom" ],
        newProduct: ''
    }
}
}
</script>

<style>

</style>