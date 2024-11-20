# layouts/cover.vue
<template>
  <div class="slidev-layout cover relative h-full w-full">
    <!-- Header -->
    <header class="absolute text-xs top-0 text-xs left-0 right-0 p-2 flex justify-between items-center">
      <div class="names">{{ $slidev.configs.author || 'Author Name' }}</div>
      <div class="date">{{ new Date().toLocaleDateString() }}</div>
    </header>

    <!-- Main content centered -->
    <div class="grid text-sm h-full place-content-center text-center">
      <slot />
    </div>

    <!-- Footer -->
    <footer class="absolute text-xs text-xs bottom-0 left-0 right-0 p-2 flex justify-between items-center">
      <div></div>
      <div class="presentation-name text-center">{{ $slidev.configs.title }}</div>
      <div></div>
    </footer>
  </div>
</template>

<style>
.slidev-layout.cover {
  @apply px-14 py-10;
}

/* Optional: Add a gradient overlay if you use background images */
.slidev-layout.cover {
  background-color: rgba(0, 0, 0, 0.4);
  background-blend-mode: overlay;
}

/* Make titles more prominent on cover */
.slidev-layout.cover h1 {
  @apply text-6xl font-bold mb-4;
}

/* Style subtitles or additional text */
.slidev-layout.cover .text-xl {
  @apply opacity-80;
}
</style>