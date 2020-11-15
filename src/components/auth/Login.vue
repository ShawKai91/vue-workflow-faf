<template>
  <div class="Login">
    <form>
      <input type="text" v-model="email">
      <input type="password" v-model="password">
    </form>

    <button @click.prevent="updateLoginDetails">Login</button>
  </div>
</template>

<script>
export default {
  name: 'Login',
  data() {
    return {
      email: '',
      password: ''
    }
  },

  // beforeUpdate() {console.log("beforeUpdate from Login");},
  // updated() {console.log("updated from Login");},

  methods: {
    updateLoginDetails() {
      this.$emit('update', this.email);
    }
  }
}
</script>

<style scoped>
</style> 