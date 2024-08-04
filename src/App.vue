<template>
  <main
    class="app dark:prose-invert mx-auto max-w-[80ch] px-6 py-[8vh] xl:text-lg"
    p="x-4 y-10"
    text="dark:gray-200"
    font-sans
  >
    <RouterView />
  </main>
</template>

<style>
html,
body {
  background: #212121 !important;
  color-scheme: dark;
  line-height: 1;
}
</style>
