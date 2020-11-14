<template>
  <div>
    <HomepageContent />

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
      password: ''
    }
  },
  components: {
    HomepageContent
  }
}
</script>

<style scoped>
</style> 