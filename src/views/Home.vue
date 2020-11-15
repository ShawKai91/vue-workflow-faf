<template>
  <div class="Home">
    <HomepageContent :subtitle="subtitleContent" :marketingMessage="marketingMessage" />
    <Auth @update="handleLoginUpdate" />
    <Auth @update="handleLoginUpdate" />
  </div>
</template>

<script>
import HomepageContent from '@/components/content/HomepageContent';
import Auth from '@/components/auth/Auth';
export default {
  name: 'home',
  data() {
    return {
      email: '',
      password: '',
      subtitleContent: "Manage your development projects.",
      marketingMessage: "Sign up today to get started for free.",
    }
  },
  components: {
    HomepageContent,
    Auth
  },
  methods: {
    handleLoginUpdate(data) {
      console.log("updated", data)
    }
  }
}
</script>