<template>
  <div class="Auth">
    <form>
      {{ formType }}

      <div v-if="formType === 'sign-up'" class="form__Name">
        <label>Name</label>
        <input type="text" v-model="name">
      </div>

      <div class="form__Email">
        <label>Email</label>
        <input type="text" v-model="email">
      </div>

      <div class="form__Password">
        <label>Password</label>
        <input type="password" v-model="password">
      </div>

    </form>

    <button @click.prevent="updateLoginDetails">Login</button>
  </div>
</template>

<script>
export default {
  name: 'Auth',
  data() {
    return {
      email: '',
      password: '',
      name: ''
    }
  },
  props: {
    formType: String
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