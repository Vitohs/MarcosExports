<template>
  <header-app />
  <v-main>
    <router-view />
  </v-main>
  <footerApp />
</template>

<script setup>
  import footerApp from '@/components/footerApp.vue'
  import headerApp from '@/components/headerApp.vue'
</script>
