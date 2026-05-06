<template>
  <header-app />
  <v-main>
    <router-view />
  </v-main>
  <footerApp />
  <language-switcher-fixed />
</template>

<script setup>
  import footerApp from '@/components/footerApp.vue'
  import headerApp from '@/components/headerApp.vue'
  import languageSwitcherFixed from '@/components/languageSwitcherFixed.vue'
</script>
