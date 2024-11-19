<template>
  <div class="slidev-layout relative h-full">
    <!-- Header with names and date -->
    <header class="absolute top-0 left-0 right-0 p-4 flex justify-between items-center">
      <div class="names">{{ $slidev.configs.author || 'Author Name' }}</div>
      <div class="date">{{ new Date().toLocaleDateString() }}</div>
    </header>

    <!-- Main content -->
    <div class="mt-16 mb-16">
      <slot />
    </div>

    <!-- Footer with presentation name and page number -->
    <footer class="absolute bottom-0 left-0 right-0 p-4 flex justify-between items-center">
      <div></div> <!-- Empty div for spacing -->
      <div class="presentation-name text-center">
        {{ $slidev.configs.title || 'Presentation Title' }}
      </div>
      <div class="page-number">{{ $slidev.nav.currentPage }} / {{ $slidev.nav.total }}</div>
    </footer>
  </div>
</template>

<style>
.slidev-layout {
  @apply px-14 py-10;
}

header, footer {
  @apply text-sm opacity-75;
}

.presentation-name {
  @apply mx-auto;
}
</style>