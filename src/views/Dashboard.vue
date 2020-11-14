<template>
  <div>
    <HomepageContent :subtitle="subtitleContent" :marketingMessage="marketingMessage" />
    <Login @update="handleLoginUpdate" />
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
      marketingMessage: "Sign up today to get started for free."
    }
  },
  components: {
    HomepageContent,
    Login
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