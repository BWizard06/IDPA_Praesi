<template>
  <div class="slidev-layout cover relative h-full w-full"
    :style="{ 
      backgroundImage: $slidev.configs.background ? `url(${$slidev.configs.background})` : 'none',
      backgroundSize: 'cover',
      backgroundPosition: 'center'
    }">
    <!-- Optional dark overlay for better text readability -->
    <div class="absolute inset-0 bg-black opacity-30" v-if="$slidev.configs.background"></div>

    <!-- Header -->
    <header class="absolute top-0 text-xs left-0 right-0 p-4 flex justify-between items-center z-10">
      <div class="names text-white">{{ $slidev.configs.author || 'Author Name' }}</div>
      <div class="date text-white">{{ new Date().toLocaleDateString() }}</div>
    </header>

    <!-- Main content centered -->
    <div class="grid h-full place-content-center text-center relative z-10">
      <slot />
    </div>

    <!-- Footer -->
    <footer class="absolute text-xs bottom-0 left-0 right-0 p-4 flex justify-between items-center z-10">
      <div></div>
      <div class="presentation-name text-center text-white">{{ $slidev.configs.title }}</div>
      <div></div>
    </footer>
  </div>
</template>

<style>
.slidev-layout.cover {
  @apply px-14 py-10;
}

/* Make text white when background image is present */
.slidev-layout.cover :deep(h1),
.slidev-layout.cover :deep(h2),
.slidev-layout.cover :deep(p) {
  @apply text-white;
}
</style>