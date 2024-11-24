<template>
  <div class="slidev-layout cover relative h-full w-full">
    <!-- Background image -->
    <img 
      v-if="$frontmatter.image" 
      :src="$frontmatter.image" 
      alt="Background"
      class="absolute inset-0 w-full h-full object-cover z-0"
    />

    <!-- Header -->
    <header class="absolute text-xs top-0 left-0 right-0 p-2 flex justify-between items-center z-10">
      <div class="names">{{ $slidev.configs.author || 'Author Name' }}</div>
      <div class="date">{{ new Date().toLocaleDateString() }}</div>
    </header>

    <!-- Main content centered -->
    <div class="grid h-full place-content-center text-center relative z-10">
      <slot />
    </div>

    <!-- Footer -->
    <footer class="absolute bottom-0 text-xs left-0 right-0 p-2 flex justify-between items-center z-10">
      <div></div>
      <div class="presentation-name text-center">{{ $slidev.configs.title }}</div>
      <div></div>
    </footer>
  </div>
</template>

<style>
.slidev-layout.cover {
  @apply relative h-full w-full;
}

.slidev-layout.cover img {
  @apply absolute inset-0 w-full h-full object-cover;
}
</style>

