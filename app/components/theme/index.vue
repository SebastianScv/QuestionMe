<template>
  <div @click="onThemeIconClick" class="flex">
    <Icon :name="themeIconName" class="cursor-pointer" />
    <!-- <h1>Color mode: {{ colorMode.value }}</h1>
    <select v-model="colorMode.preference">
      <option value="system">System</option>
      <option value="light">Light</option>
      <option value="dark">Dark</option>
      <option value="sepia">Sepia</option>
    </select> -->
  </div>
</template>

<script setup>
import { computed } from "vue";

const colorMode = useColorMode();

const themeIconName = computed(() => {
  return colorMode.value === "light"
    ? "grommet-icons:moon"
    : "grommet-icons:sun";
});

const onThemeIconClick = () => {
  colorMode.preference = colorMode.value === "light" ? "dark" : "light";
};
</script>
