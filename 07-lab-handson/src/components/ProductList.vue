<template>
  <div>
      <h2>Product List</h2>
      <ul>
          <li v-for='(i, index) in product' v-bind:key='index'>
              {{i}}
            </li>
        </ul>
  </div>
</template>

<script>


export default {
data: function(){
    return{
        product: ["Handbags", "Vacuum Cleaner" ]
    }
}
}
</script>

<style>

</style>