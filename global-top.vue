<template>
  <Frankfurt />
  <LogoHeader v-if="!isCoverSlide" />
  <InfoLine v-if="$slidev.configs.infoLine ?? true" />
</template>

<script setup lang="ts">
import { computed } from "vue";

const isCoverSlide = computed(() => {
  const currentSlide = $slidev.nav.currentPage;
  return currentSlide === 1;
});
</script>
