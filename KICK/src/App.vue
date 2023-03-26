<script setup>
import AppNavigation from './components/KICK/AppNavigation.vue'
import AppSidebar from './components/KICK/AppSideBar.vue'
import AppContent from './components/KICK/AppContent.vue'


</script>

<template>
  <AppNavigation></AppNavigation>
  <div class="content">
    <AppSidebar></AppSidebar>
    <AppContent></AppContent>
  </div>
</template>

<style scoped>

.content {
  display: flex;
}


</style>
