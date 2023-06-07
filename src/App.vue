<script setup>
import { RouterView } from 'vue-router'
import VTransitionFade from './components/VTransitionFade.vue'
import TheFooter from './layouts/TheFooter.vue'
import TheHeader from './layouts/TheHeader.vue'
</script>

<template>
  <TheHeader />
  <router-view v-slot="{ Component }">
    <VTransitionFade>
      <component :is="Component" />
    </VTransitionFade>
  </router-view>
  <TheFooter />
</template>
