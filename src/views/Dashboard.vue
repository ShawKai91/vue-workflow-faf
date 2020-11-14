<template>
  <div>
    <HomepageContent :subtitle="subtitleContent" :marketingMessage="marketingMessage" />

    <div>
      <form>
        <input type="text" v-model="email">
        <input type="password" v-model="password">
      </form>
    </div>
  </div>
</template>

<script>
import HomepageContent from '@/components/content/HomepageContent';

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
    HomepageContent
  }
}
</script>

<style scoped>
</style> 