<template>
    <div>
        <button v-on:click='random'>click</button>
        <p v-if='randomNumber%2!==0 || randomNumber===0'>{{randomNumber}}</p>
        <p v-else>{{randomNumber}}!</p>
    </div>
</template>

<script>


export default {
    data: function(){
        return{
            randomNumber: 0
        }


        
    },

    methods: {
        random: function(){
           this.randomNumber = Math.floor(Math.random() * (6-1) +  1)
        }
    }
}
</script>

<style scoped>

</style>