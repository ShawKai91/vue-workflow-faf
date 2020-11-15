<template>
  <div class="Auth">
    <form>
      {{ formattedTitle }}

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

    <button @click.prevent="updateLoginDetails">{{ formattedTitle }}</button>
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

  computed: {
    formattedTitle: function() {
      return this.formType[0].toUpperCase() + this.formType.slice(1);
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