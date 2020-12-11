<template>
  <div>
      <div>
      <h2>Product List</h2>
      <ul>
          <li v-for='(i, index) in product' v-bind:key='index'>
              {{i}}
              <button v-on:click='deleteButton(i)'>X</button>
              <button v-on:click='editButton(index)'>edit</button>
            </li>
        </ul>
        </div>
  <div>
      <label>Enter new product:</label>
      <input type='text' v-model='newProduct'>
      <button v-on:click='addButton'>Add</button>
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
    },
    methods:{
        addButton: function(){
            this.product.push(this.newProduct);
            this.newProduct = ''

        },
        deleteButton: function(i){
            let indexDelete = this.product.indexOf(i);
            this.product.splice(indexDelete,1)
        },
        editButton: function(index){
            let newProductname = prompt('Enter new prodcut')
            this.$set(this.product, index, newProductname)
        }
}
}
</script>

<style>

</style>