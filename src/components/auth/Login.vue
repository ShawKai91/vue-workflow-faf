<template>
  <div>
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
  methods: {
    updateLoginDetails() {
      this.$emit('update', this.email);
    }
  }
}
</script>

<style scoped>
</style> 