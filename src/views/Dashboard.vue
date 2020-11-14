<template>
  <div>
    <HomepageContent :subtitle="subtitleContent" :marketingMessage="marketingMessage" />
    <Login @update="handleLoginUpdate" />
    <input type="text" v-model="subdomain">

  </div>
</template>

<script>
import HomepageContent from '@/components/content/HomepageContent';
import Login from '@/components/auth/Login';

export default {
  name: 'Dashboard',
  data() {
    return {
      email: '',
       password: '',
      subtitleContent: "Manage your development projects.",
      marketingMessage: "Sign up today to get started for free.",
      subdomain: ''
    }
  },
  components: {
    HomepageContent,
    Login
  },

  beforeCreate() {console.log("beforeCreate");},
  created() {console.log("created");},

  beforeMount() {console.log("beforeMount");},
  mounted() {console.log("mounted");},

  beforeUpdate() {console.log("beforeUpdate");},
  updated() {console.log("updated");},

  beforeUnmount() {console.log("beforedestroy");},
  unmounted() {console.log("destroyed");},

  beforeRouteEnter(to, from, next) {
    const loggedIn = true;
    if (loggedIn) {next()} else {next('/')}
  },
  beforeRouteLeave(to, from, next) {
    const answer = window.confirm("Are you sure, your changes won't be saved...");
    if (answer) {next()} else {next(false)}
  },

  methods: {
    handleLoginUpdate(data) {
      console.log("dashboard login data", data);
    }
  }
}
</script>

<style scoped>
</style> 