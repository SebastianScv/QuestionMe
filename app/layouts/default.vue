<template>
  <div>
    <the-header />
    <slot />
  </div>
</template>

<script setup>
import TheHeader from "@/components/layout/the-header.vue";
</script>

<style>
body {
  @apply bg-primary dark:bg-primary-dark text-text dark:text-text-dark;
}
</style>
