<template>
  <base-card>
    <div class="flex items-center justify-center text-lg font-semibold">
      Please pick a category to start the question drill!
    </div>

    <div class="flex base-bard-item p-4 items-center gap-4">
      <Icon name="vscode-icons:file-type-node" size="40"></Icon>
      <div class="text-2xl">Java Script</div>
    </div>
  </base-card>
</template>

<style scoped>
.base-bard-item {
  @apply w-60 rounded bg-primary dark:bg-primary-dark hover:bg-[red];
}
</style>
