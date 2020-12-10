<template>
  <div>
    <div>
      <h2>please enter your username:</h2>
      <input type="text" v-model="user" /><p>{{ tooshort }}</p>
      
      <h2>please enter your password:</h2>
      <input type="text" v-model="password" /><p>{{ symbols }}</p>
      
    </div>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      user: "",
      password: "",
    };
  },
  computed: {
    tooshort: function () {
      if (this.user.length >= 7) {
        return true;
      } else {
        return false;
      }
    },
    symbols: function () {
        let specialCharacters = "~!@#$%^&^*()"
        for (let c of specialCharacters){
            if(this.password.includes(c)){
                return true;
            }
        }
        return false;
    },
  },
};
</script>

<style scoped>
</style>