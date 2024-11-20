<template>
  <div class="slidev-layout relative h-full">
    <!-- Header -->
    <header class="absolute top-0 text-xs left-0 right-0 p-2 flex justify-between items-center">
      <div class="names">{{ $slidev.configs.author || 'Author Name' }}</div>
      <div class="date">{{ new Date().toLocaleDateString() }}</div>
    </header>

    <!-- Main content with title and body -->
    <div class="content-wrapper mt-4 mb-16">
      <p class="text-2xl mb-2"><slot name="title"/></p>
      <div class="content text-sm"><slot name="content"/></div>
    </div>

    <!-- Footer -->
    <footer class="absolute text-xs bottom-0 left-0 right-0 p-2 flex justify-between items-center">
      <div></div>
      <div class="presentation-name text-center">{{ $slidev.configs.title }}</div>
      <div></div>
    </footer>
  </div>
</template>

<style>
.slidev-layout {
  @apply px-14 py-10;
}

.content-wrapper {
  @apply flex flex-col h-[calc(100%-8rem)];
}

.content {
  @apply flex-1 overflow-auto;
}
</style>