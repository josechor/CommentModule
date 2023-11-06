<script setup lang="ts">
import MainContent from './components/MainContent.vue'
</script>

<template>
  <div class="appContainer"><MainContent> </MainContent></div>
</template>

<style scoped>
.appContainer {
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  width: 100%;
}
</style>
