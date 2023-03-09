<template>
  <div @click="onThemeIconClick" class="flex">
    <Icon :name="themeIconName" class="cursor-pointer" />
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
